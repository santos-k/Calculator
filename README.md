# Calculator
Calculator in Python using Tkinter module.

from tkinter import *
root = Tk()
root.geometry("350x523")
root.title("Calculator")
color = "#1c202a"
root.config(bg=color)
top_frame = Frame(root,bg=color)
top_frame.pack()
def settext(text):
    set_val = 0
    operator1 = ""
    val = text_entry.get()
    if text == "Del" or text == "C":
        if text == "Del" or text == "CE":
            val = text_entry.get()
            n = len(val)
            str = val[:(n-1)]
            text_entry.set(str)
        elif text == "C":
            text_entry.set(0)
            text_entry2.set("")
    else:
        text_entry.set(val+text)
    if text == "=":
        try:
            get_val = text_entry.get()
            text_entry2.set(get_val)
            eval_val = get_val[:(len(get_val)-1)]
            calc = eval(eval_val)
            text_entry.set(calc)
        except:
            text_entry.set("")
            text_entry2.set("")

text_entry = StringVar()
text_entry2 = StringVar()

Label(top_frame, text="Standard Calculator",font="arial 15 bold",bg=color,fg="white").pack(fill=X,padx=3,pady=5)
entry_field1 = Entry(top_frame,font="arial 15 bold",bg=color,fg="white",textvariable=text_entry2).pack(padx=3,fill='both')
entry_field2 = Entry(top_frame,font="arial 35 bold",bg=color,fg="white",textvariable=text_entry).pack(padx=3)

bottom_frame =Frame(root,bg=color)
bottom_frame.pack(fill='both')

first_col = Frame(bottom_frame, bg=color)
first_col.pack(side='left',pady=10,padx=5,fill='both')
second_col = Frame(bottom_frame,bg=color)
second_col.pack(side='left',padx=5,pady=10,fill='both')
third_col = Frame(bottom_frame, bg=color)
third_col.pack(side='left',padx=5,pady=10,fill='both')
forth_col = Frame(bottom_frame, bg=color)
forth_col.pack(side='left',padx=5,pady=10,fill='both')
x = 4
y = 9
but_color = "#313238" #button color
but_fb_clr ="#e4e4e4" #font color
active_bg_clr = "#393c43" #button backgrounf color after click

Button(first_col,text="C",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("C")).pack(padx=2,pady=2)
Button(first_col,text=7,height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("7")).pack(padx=2,pady=2)
Button(first_col,text="4",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("4")).pack(padx=2,pady=2)
Button(first_col,text="1",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("1")).pack(padx=2,pady=2)
Button(first_col,text="00",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("00")).pack(padx=2,pady=2)
Button(second_col,text="/",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("/")).pack(padx=2,pady=2)
Button(second_col,text="8",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("8")).pack(padx=2,pady=2)
Button(second_col,text="5",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("5")).pack(padx=2,pady=2)
Button(second_col,text="2",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("2")).pack(padx=2,pady=2)
Button(second_col,text="0",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("0")).pack(padx=2,pady=2)
Button(third_col,text="*",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("*")).pack(padx=2,pady=2)
Button(third_col,text="9",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("9")).pack(padx=2,pady=2)
Button(third_col,text="6",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("6")).pack(padx=2,pady=2)
Button(third_col,text="3",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("3")).pack(padx=2,pady=2)
Button(third_col,text=".",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext(".")).pack(padx=2,pady=2)
Button(forth_col,text="Del",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("Del")).pack(padx=2,pady=2)
Button(forth_col,text="-",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("-")).pack(padx=2,pady=2)
Button(forth_col,text="+",height=x,width=y,bg=but_color,fg=but_fb_clr,activebackground=active_bg_clr,activeforeground=but_fb_clr,command= lambda:settext("+")).pack(padx=2,pady=2)
Button(forth_col,text="=",height=9,width=y,bg="#4cc2ff",command= lambda:settext("=")).pack(padx=2,pady=2)
root.mainloop()
