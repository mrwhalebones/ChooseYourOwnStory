# ChooseYourOwnStory
This is an educational python script template for creating an interactive story script.
Teaching Template: Creating a Choose-Your-Own Story Script

🔹 Step 1: Understanding the Modular Structure

Each chapter of the story is a separate Python file, allowing expansion without overcrowding a single script. Example structure:

story_project/
│── CYSP1.py  → The Beginning
│── CYSP2.py  → Chapter Two
│── CYSP3.py  → Another Chapter
│── CYSP765.py → The Ending

Each script connects to the next, using import statements and function calls like:

import CYSP2  # Links to the next story module
CYSP2.run_story(user_name)  # Transfers control to the next script

🔹 Step 2: Writing the First Script (CYSP1.py)

Students start by coding the first chapter, where they introduce choices and allow user interaction. Example:

#def get_user_choice(options):
#    """
#    Presents a list of choices and records the user's response.
#    Keeps prompting until a correct input is received.
#    """
#    while True:
#        print("\nWhat do you do next?")
#        for i, option in enumerate(options, 1):
#            print(f"{i}. {option}")

#        user_input = input("Enter the number of your choice: ").strip()

#        if not user_input.isdigit():
#            print("\nThat is not a choice you get to make right now. Try again.")
#            continue  

#        choice = int(user_input)

#        if 1 <= choice <= len(options):
#            return options[choice - 1]  
#        else:
#            print("\nThat is not a choice you get to make right now. Try again.")

🔹 Step 3: Introducing Loopbacks

Sometimes, a choice leads back to the beginning of the story instead of progressing. Example:

elif choice_1 == "Climb the tree":
    print("\nReality bends inward. Time resets. The universe rewrites itself.")
    print("\nRestarting...")
    import CYSP1  # Import first module
    CYSP1.main()  # Restart the script

Loopback choices force players to rethink their decisions while keeping the experience immersive.

🔹 Step 4: Linking Chapters

Each script must transition smoothly to the next part of the story:

import CYSP2  # Prepares next chapter

def run_story(user_name):
    print("\nYou step forward, feeling the universe shift around you.")
    print("\nTransitioning to the next module...")
    CYSP2.run_story(user_name)  # Moves to the next chapter

This structure ensures continuity, allowing each module to feel connected but independent.

🔹 Step 5: Testing and Refining

Encourage students to stress-test their program: ✅ Does every choice transition correctly? ✅ Does invalid input trigger a helpful error message? ✅ Do loopbacks return to the correct part of the story?

By following this template, learners gain insight into structured storytelling in programming while keeping the experience fun and interactive!

I’ll format this into a structured teaching guide that can serve as a printable resource. It will include: ✅ Lesson Objectives – What learners will gain from building this project ✅ Step-by-Step Instructions – Clear explanations for each part of the interactive story ✅ Code Examples – With annotations for easy understanding ✅ Exercises & Challenges – Activities to reinforce learning
