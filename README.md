# Household Energy Access and Usage Survey

In many rural or underserved communities, respondents do not always have the luxury of communicating directly with enumerators in a shared language. Often, a third party—such as a local student or family member—must act as an informal translator, introducing the risk of miscommunication or filtered responses.

To bridge this gap, this tool integrates multilingual support directly into the survey interface. By including common local languages (e.g., Igbo), enumerators can seamlessly switch languages to match the respondent’s preference—ensuring clarity, accuracy, and cultural sensitivity. This approach helps capture more authentic, unfiltered data while improving respondent comfort and engagement.

---

## 📋 Form Overview

This XLSForm includes:
- 🔄 **English and Igbo** translations
- 🧭 **GPS capture** with accuracy enforcement (≤10 m)
- 🔐 **Consent logic** that controls form flow
- ⭐ **1–5 rating widget** for influencing factors
- 🕒 **Auto-captured metadata** (timestamps, device ID)
- 📊 **Clean English-coded responses** for easy analysis, even when using local language interface

---

## 🎯 Purpose

This project serves as an exploration of the nuances, flexibility, and advanced capabilities of the XLSForm framework in digital survey design. Beyond basic data collection, the goal is to push the boundaries of what's possible using XLSForm logic—integrating features like:

- Multilingual interfaces
- Smart skip logic and relevance expressions
- Metadata capture and GPS enforcement
- Constraint-driven validation
- Dynamic calculations and rating widgets

By designing a real-world, multilingual energy access survey, this project demonstrates how XLSForm can be leveraged not just for simplicity, but for powerful, logic-rich tools that adapt to field realities.

---

## 💡 Key Learnings

- **XLSForm language tags must match `default_language` exactly.**  
  Avoid suffixes like `(en)` or `(ig)`—use `label::English`, `label::Igbo`.

- **KoBoToolbox will not recognize a language unless every visible question and choice has a corresponding translation** in that language column.

- **Hints and constraint messages are optional**, but when included in multiple languages, must follow the same naming rules (e.g., `hint::Igbo`).

- **GPS location accuracy can be enforced differently on Enketo vs ODK Collect**. Use `appearance` for Enketo (`capture-accuracy=10`) and `bind::jr:accuracyThreshold` for Collect.

- **Multilingual display does not affect data storage.** Responses remain in English due to the consistent use of `name` values in the choices sheet.

- **Field-list appearance only works in ODK Collect (not in web preview).** Enketo flattens all grouped questions into a long scroll view.

---

## 📂 Files

| File | Description |
|------|-------------|
| `xlsform/Household_Energy_Access_and_Usage_Survey.xlsx` | Final XLSForm for KoBoToolbox or ODK |
| `media/screenshots.png` | screenshots of form UI |
| `README.md` | This documentation |

---

## 🧪 Testing Instructions

1. Upload the `.xlsx` file to [KoBoToolbox](https://kf.kobotoolbox.org)
2. Deploy and preview in browser or Android ODK Collect
3. Toggle language at the top of the form (English ↔ Igbo)
4. Submit test data and export for analysis

---

## 📚 Resources Used

- XLSForm Official Site: https://getodk.org/xlsform/  
- Multilingual XLSForm Documentation: https://xlsform.org/en/#multiple-language-support  
- Language Subtag Registry: https://www.iana.org/assignments/language-subtag-registry/language-subtag-registry

---

## 📖 License

MIT — feel free to adapt and reuse with credit.
---

## 😊 enjoy!

``