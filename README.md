# My_Website
Clone the code

# installations
1. install streamlit
2. install requests
3. streamlit_lottie

# Base File
app.py

# Run the base 
streamlit run app.py

# changes
In app.py you can modify your details
In style floders you change the button colors
In images folders you can modify the images

import requests
import streamlit as st
from streamlit_lottie import st_lottie
from PIL import Image


# Find more emojis here: https://www.webfx.com/tools/emoji-cheat-sheet/
st.set_page_config(page_title="👨‍🎓 MsaiVignesh", layout="wide")


def load_lottieurl(url):
    r = requests.get(url)
    if r.status_code != 200:
        return None
    return r.json()


# Use local CSS
def local_css(file_name):
    with open(file_name) as f:
        st.markdown(f"<style>{f.read()}</style>", unsafe_allow_html=True)


local_css("style/style.css")

# ---- LOAD ASSETS ----
lottie_coding = load_lottieurl("https://assets5.lottiefiles.com/packages/lf20_fcfjwiyb.json")
img_lottie_animation = Image.open("images/hello.PNG")
img_lottie_animation1 = Image.open("images/heelo1.PNG")
img_lottie_animation2 = Image.open("images/carsharing.jpg")
img_lottie_animation3 = Image.open("images/he.jpg")


# ---- HEADER SECTION ----
with st.container():
    st.header("Hi, I am M.Krishna Sai Vignesh :wave:")
    st.title("A Software Developer")
    st.write(
        "Seeking a challenging position in a reputed organization where I can learn new skills leverage my learning s and to explore a wide variety of opportunities that can help me gain perspective towards new technologies"
    )
    st.subheader("[Click to view My Resume 👈](https://rb.gy/19znsv)")

# ---- Education ----
with st.container():
    st.write("---")
    left_column, right_column = st.columns(2)
    with left_column:
        st.header("EDUCATION DETAILS")
        st.subheader("B.Tech- CSE")
        st.write(
            """
            - College: Vel Tech Rangarajan Dr.Sagunthala R&D Institute of Science and Technology
            - Year: 2019-2023 
            - CGPA: 8.49
            - Location: Avadi, Chennai
           """
        )
        st.subheader("HSC- MPC")
        st.write(
            """
            - College: Sri Chaitanya Junior College
            - Year: 2017-2019 
            - CGPA: 9.15
            - Location: Vijayawada, Andhra Pradesh
            """
        )
        
        st.subheader("SSC- State Board")
        st.write(
            """
            - College: Montessori E.M High School
            - Year: 2016-2017
            - CGPA: 9.3
            - Location: Kurnool, Andhra Pradesh
            """
        )
    with right_column:
        st_lottie(lottie_coding, height=500, key="coding")
        
# ---- Tech Stack ----
with st.container():
    st.write("---")
    left_column, right_column = st.columns(2)
    with left_column:
        st.header("Tech Stack")
        st.write(
            """
            - Programming: Java,Spring-boot,JPA,Hibernate,Python
            - Web Development: Html,Css,JS,React
            - IDE's: Colab, Pycharm, pring Tool Suite,Visual Studio, Eclipse
           """
        )
        
        
# ---- InternShips ----
with st.container():
    st.write("---")
    left_column, right_column = st.columns(2)
    with left_column:
        st.header("Internships")
        st.subheader("Full Stack Developer Internship")
        st.write(
            """
            - Company: Virtusa
            - Duration: 2022-Jun to 2023-Jul
           """
        )
        
        st.subheader("HR - Coordinator Internship")
        st.write(
            """
            - Company: Startup World and Smart cookie pvt ltd
            - Duration: 2022-Nov to 2023-Apr
           """
        )
        st.subheader("HR & Trainer")
        st.write(
            """
            - Company: InfySkill Edutech pvt ltd
            - Duration: 2023-Jan
           """
        )

# ---- PROJECTS ----
with st.container():
    st.write("---")
    st.header("My Projects")
    st.write("##")
    image_column, text_column = st.columns((1, 2))
    with image_column:
        st.image(img_lottie_animation)
    with text_column:
        st.subheader("Phd Admission Portal")
        st.write(
            """
            - An innovative web-based Ph.D. Admission Portal built with Java and Spring Boot provides a dynamic backend.
            - while React manages an user-focused frontend, setting a new benchmark for smooth interactions.
            - Implemented secure, Spring-boot-powered RESTful APIs to the web application, enabling seamless frontend-backend connectivity.
            - A dynamic and client-server React frontend were elevating, taking user experiences to a new level of seamlessness.
            - Advanced spring-security Jwt token mechanisms were used to strengthen user authentication and authorization while protecting data privacy, and a powerful JPA Hibernate, MySql database system was integrated for faster applicant information administration.
            """
        )
        st.markdown("[GitHub Link](https://github.com/iamneo-production/97a31c2f-60fd-4cd6-aa07-369cc20f779e)")
with st.container():
    image_column, text_column = st.columns((1, 2))
    with image_column:
        st.image(img_lottie_animation1)
    with text_column:
        st.subheader("Responsive Portfolio Website")
        st.write(
            """
            - The Responsive Portfolio Website effectively combines design and usability, balancing cross device accessibility and visual attraction to boost portfolio and display skills.
            - Dedicated segments showcasing your work history, projects & achievements, with appealing pictures and insightful explanations to highlight your abilities.
            - Developed an easy-to-use navigation system that guides users through various website parts while maximizing performance using techniques like lazy loading and picture compressing.
            - Utilized meta tags, targeted keywords, and SEO upgrades to increase online presence and search engine ranking.
            """
        )
        st.markdown("[GitHub Link](https://github.com/saivigneesh456/Portfolio)")
        
with st.container():
    image_column, text_column = st.columns((1, 2))
    with image_column:
        st.image(img_lottie_animation2)
    with text_column:
        st.subheader("Ride Sharing Application")
        st.write(
            """
            - The Ride Sharing Application is a Spring Boot-based Java project that aims to improve transportation accessibility and cost effectiveness through simple ride-sharing.
            - Developed a plan for smooth integration, arranging harmonious teamwork for effective deployment.
            - Spring Boot was used to construct RESTful APIs, allowing for seamless frontend,backend communication.
            - Utilized MySQL’s capability for simplified data storage and retrieval, increasing efficiency inside the Spring Boot-powered development pipeline.
            """
        )
        st.markdown("[GitHub Link](https://github.com/iamneo-production/3fb3f3f7-99de-496a-a1a6-329afb7fcd48)")
        
with st.container():
    image_column, text_column = st.columns((1, 2))
    with image_column:
        st.image(img_lottie_animation3)
    with text_column:
        st.subheader("Simple Banking Application")
        st.write(
            """
            - It aims to develop a platform to manage all bank transactions.
            - It aims to develop a platform to manage all bank transactions, access to bank balance using Tech stack HTML, CSS, Spring Boot & MySQL.
            """
        )
        st.markdown("[GitHub Link](https://github.com/saivigneesh456/loan_backend)")
        


    
    
# ---- Certifications ----
with st.container():
    st.write("---")
    left_column, right_column = st.columns(2)
    with left_column:
        st.header("CERTIFICATIONS")
        st.write(
            """
            - Oracle certified Java SE 8 Programmer I
            - Wipro Java J2EE certification 
            - AWS Academy Machine Learning
            - Oracle Cloud Infrastructure Certified Architect Professional
            - Oracle Cloud Infrastructure Certified Architect Associate
            - AWS Academy Cloud Foundations
            - Infosus 5G certification
           """ )
    with right_column:
        st_lottie(lottie_coding, height=300, key="coding1")
        
        
        # ---- CONTACT ----
with st.container():
    st.write("---")
    st.header("Get In Touch With Me!")
    st.write("##")
    # Documention: https://formsubmit.co/ !!! CHANGE EMAIL ADDRESS !!!
    contact_form = """
    <form action="https://formsubmit.co/sai.9441051886@gmail.com" method="POST">
        <input type="hidden" name="_captcha" value="false">
        <input type="text" name="name" placeholder="Your name" required>
        <input type="email" name="email" placeholder="Your email" required>
        <textarea name="message" placeholder="Your message here" required></textarea>
        <button type="submit">Send</button>
    </form>
    """
    
    
    left_column, right_column = st.columns(2)
    with left_column:
        st.markdown(contact_form, unsafe_allow_html=True)
    with right_column:
        st.empty()
