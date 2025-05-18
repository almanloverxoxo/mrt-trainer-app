import streamlit as st

st.set_page_config(page_title="MRT Trainer", layout="centered")

st.title("🧠 MRT Trainings-Simulator")

st.write("Willkommen im MRT-Trainer. Bitte wähle eine Körperregion aus und simuliere deine Untersuchung.")

region = st.selectbox("Wähle die Untersuchungsregion:", ["Kopf", "HWS", "LWS", "Knie", "Abdomen"])

if region == "Kopf":
    st.success("Empfohlene Sequenzen: T1 axial, T2 axial, FLAIR, DWI.")
elif region == "HWS":
    st.success("Empfohlene Sequenzen: T2 sagittal, T1 axial, STIR.")
elif region == "LWS":
    st.success("Empfohlene Sequenzen: T1 sagittal, T2 sagittal, T2 axial.")
elif region == "Knie":
    st.success("Empfohlene Sequenzen: PD fat-sat, T1 coronal, T2 sagittal.")
elif region == "Abdomen":
    st.success("Empfohlene Sequenzen: T2 HASTE, T1 VIBE, Diffusion.")

st.write("---")
st.info("Hier könntest du später Sequenzen auswählen, Fehlerfeedback erhalten und Trainingsfälle laden.")
