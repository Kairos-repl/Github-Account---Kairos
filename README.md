import tkinter as tk // Dela Cruz
from tkinter import messagebox

""" This function allows us for handling menu actions """
def add_medicine():
    messagebox.showinfo("Add Medicine", "This feature will allow you to add a new medicine reminder.")

def view_schedule():
    messagebox.showinfo("View Schedule", "This feature will display the medication schedule.")

def open_settings():
    messagebox.showinfo("Settings", "This feature will allow users to configure preferences.")

def show_about():
    messagebox.showinfo("About", "Intelligent Medicine Reminder System\nVersion 1.0\nDeveloped by Drug Testers Team")

def exit_app():
    """Closes the application."""
    root.quit()

""" Main window of the app """
root = tk.Tk()
root.title("Intelligent Medicine Reminder System")
root.geometry("500x300")  # Set window size

""" Menu Bar """
menu_bar = tk.Menu(root)

""" This is the File Menu """
file_menu = tk.Menu(menu_bar, tearoff=0)
file_menu.add_command(label="Add Medicine", command=add_medicine)
file_menu.add_command(label="View Schedule", command=view_schedule)
file_menu.add_separator()
file_menu.add_command(label="Exit", command=exit_app)
menu_bar.add_cascade(label="File", menu=file_menu)

root.config(menu=menu_bar)
root.mainloop() // Dela Cruz
