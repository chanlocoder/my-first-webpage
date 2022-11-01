
import requests
import streamlit as st
from streamlit_lottie import st_lottie

st.set_page_config(page_title="my webpage",page_icon=":tada:", layout="wide")

def load_loattieur(url):
    r = requests.get(url)
    if r.status_code != 200:
        return None
    return r.json()    


lottie_coding = load_loattieur("https://assets5.lottiefiles.com/packages/lf20_SPA6bgo7nO.json")
with st.container():
  st.subheader("hi,my name is lochan")
  st.title("i am student")
  st.write("i just started learning python")
  st.write()

with st.container():
    st.write("---")  
    left_column,right_comlumn = st.columns(2)
    with left_column:
        st.header("what i do")
        st.write("##")
        st.write("I am 13 year old and i am from india.I just started learning coding")

with right_comlumn:
    st_lottie(lottie_coding,height= 300,key="coding")

with st.container():
    st.write("---")
    st.header("my projects")
    st.write("##")
    image_comlumn, text_comlumn = st.columns((1,2))
    with image_comlumn:

     with text_comlumn:
        st.write("i just started so no projects till now")
        st.write("its my first webpage and i want to make more webpage ")
            
