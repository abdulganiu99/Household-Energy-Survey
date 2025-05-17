# Household Energy Access and Usage Survey

A multilingual digital survey tool for collecting data on household electricity sources and energy usage patterns across Nigeria and Ghana.

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

This survey is designed for use in communities where respondents may only understand local languages. Enumerators can toggle the form language between **English** and **Igbo** while collecting responses that are saved in clean, English-coded format for analysis.

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
| `forms/Household_Energy_Access_and_Usage_Survey.xlsx` | Final XLSForm for KoBoToolbox or ODK |
| `media/screenshots.png` | Optional screenshots of form UI |
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
"""

# enjoy!
``