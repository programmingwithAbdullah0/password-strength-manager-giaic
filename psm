# import streamlit as st 
# import re

# #page styling
# st.set_page_config(page_title="Password Strength check my Programming with Abdullah",page_icon="Abdullah", layout="centered")

#  #custom css
# st.markdown(
#     """
#     <style>
#     .main { text-align: center; }
#     .stTextInput { width: 60%; !important; margin: auto; }
#     .stButton button { width: 50%; background-color: #4CAF50; color: white; font-size: 18px; }
#     .stButton button:hover { background-color: #45a049; }
#     </style>
#     """,
#     unsafe_allow_html=True
# )

# #page title

# st.title("Password Strength Checker")
# st.write("Enter Password to check its strength")

# #func to check password strength

# def check_password_strength(password):
#     score = 0
#     feedback = []
#     if len(password) >= 8:
#         score += 1 #score increase by 1
#     else:
#      feedback.append("Password should be **atleast 8 characters**")

# if re.search(r'[A - Z]', password and re.search(r'[a - z]', password): # type: ignore
#              score += 1
#      feedback.append("Password should contain both **lowercase** and **uppercase** letters")


#      if re.search(r"\d", password): # type: ignore
#              score += 1
#              feedback.append("Password should contain **at least one digit**")

#              #for special characters
#              if re.search(r"[!@#$%^&*(),.?':{}|<>]", password): # type: ignore
#                  score += 1
#                  feedback.append("Password should contain **at least one special character**")  

#                  #display password strength results
#                  if score == 4:
#                  st.success("Your password is secure")
#                  elif score == 3 :
#                  st.info("**Moderate password** Consider improving your password")
#                  else :
#                  st.error("**Weak Password** Follow the suggestion below to strength")

#                  #feedback
#                  if feedback:
#                  with st.expander("Improve your password")
#                  for item in feedback:
#                  st.write(item)

#                  password = st.text_input("Enter your password:", type="password", help="ensure your password is strong")

#                  #button
#                  if st.button("Check Password"):
#                  if password:
#                  check_password_strength(password)
#                  else
#                  st.warning("Please enter a password first")

import streamlit as st
import re

# Page styling
st.set_page_config(page_title="Password Strength Check by Programming with Abdullah",
                   page_icon="🔐", layout="centered")

# Custom CSS
st.markdown(
    """
    <style>
    .main { text-align: center; }
    .stTextInput { width: 60% !important; }
    .stButton button { width: 50%; background-color: #4CAF50; color: white; font-size: 18px; }
    .stButton button:hover { background-color: #45a049; }
    </style>
    """,
    unsafe_allow_html=True
)

# Page title
st.title("🔐 Password Strength Checker")
st.write("Enter a password to check its strength.")

# Function to check password strength
def check_password_strength(password):
    score = 0
    feedback = []

    if len(password) >= 8:
        score += 1
    else:
        feedback.append("Password should be **at least 8 characters** long.")

    if re.search(r'[A-Z]', password) and re.search(r'[a-z]', password):  # Corrected regex
        score += 1
    else:
        feedback.append("Password should contain both **lowercase** and **uppercase** letters.")

    if re.search(r"\d", password):  # Check for numbers
        score += 1
    else:
        feedback.append("Password should contain **at least one digit**.")

    if re.search(r"[!@#$%^&*(),.?':{}|<>]", password):  # Check for special characters
        score += 1
    else:
        feedback.append("Password should contain **at least one special character**.")

    # Display password strength results
    if score == 4:
        st.success("✅ Your password is **Secure**!")
    elif score == 3:
        st.info("🟡 **Moderate password** - Consider improving it.")
    else:
        st.error("❌ **Weak Password** - Follow the suggestions below.")

    # Show improvement suggestions
    if feedback:
        with st.expander("💡 Improve Your Password"):
            for item in feedback:
                st.write("🔸 " + item)

# Input field
password = st.text_input("Enter your password:", type="password", help="Ensure your password is strong.")

# Check button
if st.button("🔍 Check Password"):
    if password:
        check_password_strength(password)
    else:
        st.warning("⚠️ Please enter a password first.")
