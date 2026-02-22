# 📂 Data Folder

## ⚠️ Dataset Not Included

The original dataset (`Student.xlsx`) is **not included** in this repository as it may contain sensitive student records.

---

## 📋 Dataset Schema

Place your `Student.xlsx` file here with the sheet named **"University information"**.

The dataset should contain the following columns:

### 👤 Demographic Features
| Column | Description |
|---|---|
| `STUDENT IDENTIFIER` | Unique student ID |
| `STDNT_AGE` | Student age |
| `STDNT_GENDER` | Gender (M/F) |
| `STDNT_BACKGROUND` | Background category |
| `IN_STATE_FLAG` | In-state student (Y/N) |
| `INTERNATIONAL_STS` | International student (Y/N) |
| `DISTANCE_FROM_HOME` | Distance from home to university |
| `HOUSING_STS` | Housing status |

### 🏫 Academic Background
| Column | Description |
|---|---|
| `HIGH_SCHL_GPA` | High school GPA |
| `HIGH_SCHL_NAME` | High school name |
| `STDNT_MAJOR` | Major field of study |
| `STDNT_MINOR` | Minor field of study |
| `STDNT_TEST_ENTRANCE1` | Entrance exam score 1 |
| `STDNT_TEST_ENTRANCE2` | Entrance exam score 2 |
| `STDNT_TEST_ENTRANCE_COMB` | Combined entrance score |
| `DEGREE_GROUP_CD` | Degree group code |
| `DEGREE_GROUP_DESC` | Degree group description |

### 📚 First Term Performance
| Column | Description |
|---|---|
| `FIRST_TERM_ATTEMPT_HRS` | Credit hours attempted |
| `FIRST_TERM_EARNED_HRS` | Credit hours earned |
| `CORE_COURSE_NAME_1_F` to `CORE_COURSE_NAME_6_F` | Course names (Fall) |
| `CORE_COURSE_GRADE_1_F` to `CORE_COURSE_GRADE_6_F` | Course grades (Fall) |

### 📖 Second Term Performance
| Column | Description |
|---|---|
| `SECOND_TERM_ATTEMPT_HRS` | Credit hours attempted |
| `SECOND_TERM_EARNED_HRS` | Credit hours earned |
| `CORE_COURSE_NAME_1_S` to `CORE_COURSE_NAME_6_S` | Course names (Spring) |
| `CORE_COURSE_GRADE_1_S` to `CORE_COURSE_GRADE_6_S` | Course grades (Spring) |

### 💰 Financial Features
| Column | Description |
|---|---|
| `GROSS_FIN_NEED` | Gross financial need |
| `COST_OF_ATTEND` | Total cost of attendance |
| `EST_FAM_CONTRIBUTION` | Estimated family contribution |
| `UNMET_NEED` | Unmet financial need |

### 🎯 Target Variable
| Column | Description |
|---|---|
| `RETURNED_2ND_YR` | 1 = Returned, 0 = Did not return |

---

## 📌 Notes

- Grades are letter grades: A, A-, B+, B, B-, C+, C, C-, D, F
- The notebook converts letter grades to a 4.0 GPA scale
- Missing values are handled via median imputation (numerical) and context-aware random imputation (entrance scores)
