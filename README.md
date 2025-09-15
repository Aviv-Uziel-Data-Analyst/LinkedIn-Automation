# אוטומציה בלינקדאין - מדריך מלא

clay link: 
https://www.clay.com/

LGM link:
https://lagrowthmachine.com/

random id formula: 
Math.random().toString(36).slice(2)+Date.now().toString(36)

Clay search lead run condition:
{{first_name_hebrew}}?.translation?.translatedText && {{LinkedIn Profile}}

Clay create lead run condition:
!{{Search Lead}} && {{Company Name}} && {{LinkedIn Profile}}

<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>מדריך אוטומציה בלינקדאין</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: #24292f;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #ffffff;
            direction: rtl;
        }
        
        .header {
            background: linear-gradient(135deg, #0077b5, #00a0dc);
            color: white;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .header h1 {
            margin: 0;
            font-size: 2.5em;
            font-weight: 600;
        }
        
        .header p {
            margin: 10px 0 0 0;
            font-size: 1.2em;
            opacity: 0.9;
        }
        
        .overview {
            background-color: #f6f8fa;
            border: 1px solid #d0d7de;
            border-radius: 8px;
            padding: 25px;
            margin-bottom: 30px;
        }
        
        .overview h2 {
            color: #0969da;
            margin-top: 0;
            border-bottom: 2px solid #0969da;
            padding-bottom: 10px;
        }
        
        .prerequisites {
            background-color: #fff8c5;
            border-right: 4px solid #f9c23c;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px 0 0 8px;
        }
        
        .prerequisites h3 {
            margin-top: 0;
            color: #7d4e00;
        }
        
        .step-section {
            background-color: #ffffff;
            border: 1px solid #d0d7de;
            border-radius: 8px;
            margin-bottom: 30px;
            overflow: hidden;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
        }
        
        .step-header {
            background-color: #f6f8fa;
            padding: 20px 25px;
            border-bottom: 1px solid #d0d7de;
        }
        
        .step-header h2 {
            margin: 0;
            color: #24292f;
            font-size: 1.5em;
            display: flex;
            align-items: center;
        }
        
        .step-number {
            background-color: #0969da;
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-left: 15px;
            font-size: 0.9em;
        }
        
        .step-content {
            padding: 25px;
        }
        
        .substep {
            background-color: #f8f9fa;
            border-right: 3px solid #0969da;
            padding: 20px;
            margin: 20px 0;
            border-radius: 6px 0 0 6px;
        }
        
        .substep h4 {
            margin-top: 0;
            color: #0969da;
            font-size: 1.1em;
        }
        
        .image-placeholder {
            background-color: #f6f8fa;
            border: 2px dashed #d0d7de;
            border-radius: 8px;
            padding: 30px;
            text-align: center;
            margin: 15px 0;
            color: #656d76;
            font-style: italic;
        }
        
        .platform-link {
            display: inline-block;
            background-color: #0969da;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 6px;
            font-weight: 500;
            margin: 5px 0 5px 10px;
            transition: background-color 0.2s;
        }
        
        .platform-link:hover {
            background-color: #0550ae;
        }
        
        .code-snippet {
            background-color: #f6f8fa;
            border: 1px solid #d0d7de;
            border-radius: 6px;
            padding: 15px;
            font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
            font-size: 0.9em;
            margin: 15px 0;
            overflow-x: auto;
            direction: ltr;
            text-align: left;
        }
        
        .warning {
            background-color: #fff1f0;
            border-right: 4px solid #da3633;
            padding: 15px;
            margin: 15px 0;
            border-radius: 6px 0 0 6px;
        }
        
        .warning strong {
            color: #cf222e;
        }
        
        .success {
            background-color: #f0fff4;
            border-right: 4px solid #2da44e;
            padding: 15px;
            margin: 15px 0;
            border-radius: 6px 0 0 6px;
        }
        
        .success strong {
            color: #1a7f37;
        }
        
        .workflow-diagram {
            text-align: center;
            margin: 30px 0;
            padding: 20px;
            background-color: #f6f8fa;
            border-radius: 8px;
        }
        
        ul, ol {
            padding-right: 20px;
        }
        
        li {
            margin-bottom: 8px;
        }
        
        .footer {
            background-color: #24292f;
            color: #f0f6fc;
            padding: 25px;
            border-radius: 8px;
            text-align: center;
            margin-top: 40px;
        }
    </style>
</head>
<body>

<div class="header">
    <h1>🚀 [translate:אוטומציה בלינקדאין]</h1>
    <p>[translate:מדריך מלא לייצור לידים אוטומטי ויצירת קשר ממוקדת]</p>
</div>

<div class="overview">
    <h2>🎯 [translate:סקירת הפרויקט]</h2>
    <p>[translate:מדריך מקיף זה מדגים כיצד לבנות פייפליין אוטומטי ליצירת קשר בלינקדאין באמצעות] <strong>Clay.com</strong> [translate:לייצור לידים חכם ו-] <strong>LaGrowthMachine (LGM)</strong> [translate:להרצת קמפיינים אוטומטיים. המערכת פותחה כחלק מאסטרטגיית חיפוש עבודה מתקדמת, המשלבת מומחיות בניתוח נתונים עם פלטפורמות אוטומציה שיווקיות.]</p>
    
    <div class="workflow-diagram">
        <h3>🔄 [translate:זרימת העבודה האוטומטית]</h3>
        <p><strong>[translate:לינקדאין ← Clay (ייצור לידים) ← LaGrowthMachine (אוטומציה) ← יצירת קשר ממוקדת]</strong></p>
    </div>
    
    <p><strong>[translate:פלטפורמות עיקריות בשימוש:]</strong></p>
    <a href="https://www.clay.com/" class="platform-link" target="_blank">Clay.com</a>
    <a href="https://lagrowthmachine.com/" class="platform-link" target="_blank">LaGrowthMachine</a>
</div>

<div class="prerequisites">
    <h3>📋 [translate:דרישות מוקדמות]</h3>
    <ul>
        <li>[translate:חשבון לינקדאין פעיל (מומלץ LinkedIn Sales Navigator)]</li>
        <li>[translate:חשבון Clay.com עם גישה ל-API]</li>
        <li>[translate:חשבון LaGrowthMachine (LGM)]</li>
        <li>[translate:הבנה בסיסית של זרימות עבודה אוטומטיות]</li>
        <li>[translate:הגדרת קהל יעד ופרופיל לקוח אידיאלי]</li>
    </ul>
</div>

<!-- Step 1: LGM Audience Creation -->
<section class="step-section">
    <div class="step-header">
        <h2><span class="step-number">1</span>[translate:LaGrowthMachine - יצירת קהל יעד]</h2>
    </div>
    <div class="step-content">
        <p>[translate:התחל בהגדרת קהל היעד שלך ב-LaGrowthMachine. שלב יסודי זה מגדיר למי האוטומציה שלך תגיע ומבטיח שהקמפיינים שלך מתמקדים בפרוספקטים הנכונים.]</p>
        
        <h3>🎯 [translate:תהליך הגדרת הקהל]</h3>
        
        <div class="substep">
            <h4>[translate:ניווט ליצירת קהל]</h4>
            <p>[translate:גש ללוח הבקרה של LaGrowthMachine ומצא את חלק יצירת הקהל. כאן תגדיר את פרופיל הלקוח האידיאלי שלך ופרמטרי המיקוד.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 1.0_LGM_create_audience/2025-09-15 16 33 22.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הגדרת פרמטרי קהל]</h4>
            <p>[translate:הגדר את קריטריוני קהל היעד שלך כולל תפקידים, תעשיות, גדלי חברות ומיקומים גיאוגרפיים. היה ספציפי כדי להבטיח לידים איכותיים התואמים לפרופיל הלקוח האידיאלי שלך.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 1.0_LGM_create_audience/2025-09-15 16 33 36.png]
            </div>
            
            <div class="success">
                <strong>[translate:טיפ מקצועי:]</strong> [translate:התחל עם קריטריוני מיקוד צרים והרחב בהדרגה בהתבסס על נתוני ביצועי הקמפיין.]
            </div>
        </div>
    </div>
</section>

<!-- Step 2: LGM API Configuration -->
<section class="step-section">
    <div class="step-header">
        <h2><span class="step-number">2</span>[translate:LaGrowthMachine - הגדרת מפתח API]</h2>
    </div>
    <div class="step-content">
        <p>[translate:הגדר את חיבור ה-API בין LaGrowthMachine לפלטפורמות חיצוניות. שלב זה חיוני לאפשר זרימת נתונים בין כלי ייצור הלידים לפלטפורמת האוטומציה.]</p>
        
        <div class="substep">
            <h4>[translate:גישה להגדרות API]</h4>
            <p>[translate:נווט לחלק הגדרת ה-API בחשבון LaGrowthMachine שלך. זה יאפשר אינטגרציה עם Clay וכלים אחרים לייצור לידים.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 1.1_LGM_api_key/2025-09-15 16 25 13.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:יצירה והגדרה של מפתח API]</h4>
            <p>[translate:צור את מפתח ה-API שלך והגדר את ההרשאות הדרושות לייבוא לידים וניהול קמפיינים. שמור מפתח זה בבטחה מכיוון שהוא ישמש באינטגרציית Clay.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 1.1_LGM_api_key/2025-09-15 16 25 27.png]
            </div>
            
            <div class="warning">
                <strong>[translate:הערת אבטחה:]</strong> [translate:לעולם אל תשתף את מפתח ה-API שלך בפומבי ושמור אותו במקום בטוח. חדש את המפתח אם אתה חושד שהוא נפגע.]
            </div>
        </div>
    </div>
</section>

<!-- Step 3: Clay Initial Setup -->
<section class="step-section">
    <div class="step-header">
        <h2><span class="step-number">3</span>[translate:פלטפורמת Clay - הגדרה ראשונית וקונפיגורציה]</h2>
    </div>
    <div class="step-content">
        <p>[translate:הגדר את סביבת העבודה שלך ב-Clay לייצור לידים והעשרת נתונים. Clay ישמש כשכבת המודיעין, ימצא ויכשיר לידים לפני שליחתם לפלטפורמת האוטומציה.]</p>
        
        <h3>🏗️ [translate:הגדרת סביבת העבודה ב-Clay]</h3>
        
        <div class="substep">
            <h4>[translate:יצירת טבלה חדשה ב-Clay]</h4>
            <p>[translate:התחל ביצירת טבלה חדשה ב-Clay שתכיל את זרימת העבודה לייצור הלידים. טבלה זו תכיל את כל שלבי עיבוד הנתונים והאינטגרציות.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 10 40.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הגדרת מקורות נתונים]</h4>
            <p>[translate:הגדר את מקורות הקלט שלך, כולל פרמטרי חיפוש בלינקדאין, מאגרי נתונים של חברות ורשימות לידים קיימות שברצונך להעשיר.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 11 06.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הגדרת אינטגרציית לינקדאין]</h4>
            <p>[translate:חבר את Clay ללינקדאין והגדר פרמטרי חיפוש. אינטגרציה זו תאפשר ל-Clay למצוא ולחלץ מידע על פרוספקטים אוטומטית.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 11 14.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 11 26.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:עמודות העשרת נתונים]</h4>
            <p>[translate:הוסף עמודות להעשרת נתונים כולל מציאת אימייל, מידע על חברות, תפקידים ופרטי יצירת קשר. הגדר כל מקור העשרה לאיכות נתונים מקסימלית.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 11 34.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 12 56.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:תרגום ולוקליזציה]</h4>
            <p>[translate:הגדר שירותי תרגום ליצירת קשר בינלאומית. זה חשוב במיוחד עבור קמפיינים רב-לשוניים או כאשר מיקדים שווקים גלובליים.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 13 23.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 13 43.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:סינון מתקדם ואימות]</h4>
            <p>[translate:הגדר מסננים מתקדמים כדי להבטיח איכות הלידים. הגדר כללי אימות עבור כתובות אימייל, מידע על חברות ורלוונטיות איש הקשר.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 14 11.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 14 45.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:העשרת נתוני חברות]</h4>
            <p>[translate:הוסף העשרת נתונים ספציפית לחברות כדי לספק הקשר לפרסונליזציה. כלול גודל חברה, תעשייה, חדשות אחרונות ומדדי צמיחה.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 15 16.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 15 56.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 15 57.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:עיצוב פלט והגדרת ייצוא]</h4>
            <p>[translate:הגדר את פורמט פלט הנתונים הסופי כדי להבטיח תאימות עם LaGrowthMachine. הגדר טריגרים לייצוא אוטומטי ואימות נתונים.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 17 22.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 17 39.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 18 19.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 18 37.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 18 51.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 19 15.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 19 32.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 2_clay setup_1/2025-09-15 16 19 46.png]
            </div>
        </div>
    </div>
</section>

<!-- Step 4: Clay Advanced Configuration -->
<section class="step-section">
    <div class="step-header">
        <h2><span class="step-number">4</span>[translate:Clay - הגדרה מתקדמת - זרימות עבודה לחיפוש ויצירת לידים]</h2>
    </div>
    <div class="step-content">
        <p>[translate:הגדר זרימות עבודה מתקדמות ב-Clay לעיבוד לידים חכם. שלב זה כולל הגדרת לוגיקה מותנית לכישור לידים ופעולות אוטומטיות בהתבסס על איכות הנתונים.]</p>
        
        <h3>🔍 [translate:זרימת עבודה לחיפוש לידים]</h3>
        
        <div class="substep">
            <h4>[translate:הגדרת חיפוש לידים]</h4>
            <p>[translate:הגדר את זרימת העבודה לחיפוש לידים כדי לזהות ולאמת פרוספקטים פוטנציאליים. זרימת עבודה זו משתמשת בלוגיקה מותנית כדי לקבוע אם יש לעבד ליד נוסף.]</p>
            
            <div class="code-snippet">
                <strong>[translate:תנאי הרצת חיפוש ליד:]</strong><br>
                {{first_name_hebrew}}?.translation?.translatedText && {{LinkedIn Profile}}
            </div>
            
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/1_seach lead/2025-09-15 16 25 53.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/1_seach lead/2025-09-15 16 26 49.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:פרמטרי אימות לידים]</h4>
            <p>[translate:הגדר כללי אימות כדי להבטיח איכות הלידים. הגדר בדיקות עבור שלמות פרופיל, ניקוד רלוונטיות ודיוק מידע יצירת קשר.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/1_seach lead/2025-09-15 16 27 37.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/1_seach lead/2025-09-15 16 27 51.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:מסנני חיפוש מתקדמים]</h4>
            <p>[translate:יישם לוגיקת סינון מתקדמת כדי לחדד את איכות הלידים ולהבטיח שרק פרוספקטים בעלי פוטנציאל גבוה ימשיכו לשלב היצירה.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/1_seach lead/2025-09-15 16 30 21.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/1_seach lead/2025-09-15 16 31 10.png]
            </div>
        </div>
        
        <h3>🏗️ [translate:זרימת עבודה ליצירת לידים]</h3>
        
        <div class="substep">
            <h4>[translate:לוגיקת יצירת לידים]</h4>
            <p>[translate:הגדר את זרימת העבודה ליצירת לידים המעבדת פרוספקטים מכושרים ומכינה אותם לייצוא ל-LaGrowthMachine. זרימת עבודה זו כוללת עיצוב נתונים ואימות סופי.]</p>
            
            <div class="code-snippet">
                <strong>[translate:תנאי הרצת יצירת ליד:]</strong><br>
                !{{Search Lead}} && {{Company Name}} && {{LinkedIn Profile}}
            </div>
            
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/2_create lead/2025-09-15 16 31 22.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/2_create lead/2025-09-15 16 31 44.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:עיצוב נתונים וסטנדרטיזציה]</h4>
            <p>[translate:הגדר כללי עיצוב נתונים כדי להבטיח עקביות בין כל הלידים. סטנדרטיזה מוסכמות שמות, פורמטי יצירת קשר ומידע על חברות.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/2_create lead/2025-09-15 16 36 00.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/2_create lead/2025-09-15 16 36 50.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הכנה סופית של לידים]</h4>
            <p>[translate:השלם את תהליך יצירת הלידים על ידי הוספת נגיעות אחרונות, נקודות נתונים לפרסונליזציה ועיצוב ייצוא לאינטגרציה חלקה עם LaGrowthMachine.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/2_create lead/2025-09-15 16 37 09.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 3_clay_setup_2/2_create lead/2025-09-15 16 38 47.png]
            </div>
        </div>
        
        <div class="success">
            <strong>[translate:הצלחת זרימת העבודה:]</strong> [translate:זרימות העבודה שלך ב-Clay מוגדרות כעת לעבד לידים בצורה חכמה עם לוגיקה מותנית ובדיקות איכות.]
        </div>
    </div>
</section>

<!-- Step 5: Lead Generation Execution -->
<section class="step-section">
    <div class="step-header">
        <h2><span class="step-number">5</span>[translate:Clay - הרצת ייצור לידים]</h2>
    </div>
    <div class="step-content">
        <p>[translate:הרץ את זרימת העבודה לייצור לידים ב-Clay ועקוב אחר התוצאות. שלב זה כולל הרצת הזרימות המוגדרות והבטחת איכות נתונים לפני ייצוא.]</p>
        
        <div class="substep">
            <h4>[translate:הרצת זרימת העבודה]</h4>
            <p>[translate:הרץ את זרימות העבודה שלך ב-Clay כדי לייצר לידים מכושרים. עקוב אחר העיבוד בזמן אמת ובדוק אם יש שגיאות או בעיות איכות נתונים.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 4_clay_generating_leads/2025-09-15 16 48 42.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:אימות תוצאות]</h4>
            <p>[translate:סקור את הלידים שנוצרו לאיכות ושלמות. ודא שכל השדות הנדרשים מאוכלסים ושהנתונים עומדים בסטנדרטים של הקמפיין שלך.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 4_clay_generating_leads/2025-09-15 16 48 58.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הערכת איכות לידים]</h4>
            <p>[translate:נתח את תוצאות ייצור הלידים, בדוק שיעורי המרה, דיוק נתונים ואיכות לידים כללית. בצע התאמות לזרימות העבודה במידת הצורך.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 4_clay_generating_leads/2025-09-15 16 49 20.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הכנת ייצוא]</h4>
            <p>[translate:הכן את הלידים המכושרים שלך לייצוא ל-LaGrowthMachine. ודא שכל הנתונים מעוצבים כראוי ועומדים בדרישות לאוטומציית קמפיינים.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 4_clay_generating_leads/2025-09-15 16 49 44.png]
            </div>
            
            <div class="code-snippet">
                <strong>[translate:נוסחת ייצור מזהה אקראי:]</strong><br>
                Math.random().toString(36).slice(2)+Date.now().toString(36)
            </div>
        </div>
    </div>
</section>

<!-- Step 6: LGM Campaign Setup -->
<section class="step-section">
    <div class="step-header">
        <h2><span class="step-number">6</span>[translate:LaGrowthMachine - הגדרת קמפיין ואוטומציה]</h2>
    </div>
    <div class="step-content">
        <p>[translate:הגדר את קמפיין יצירת הקשר האוטומטי שלך ב-LaGrowthMachine באמצעות הלידים שנוצרו מ-Clay. שלב סופי זה מחבר הכל למערכת לינקדאין אוטומטית מלאה ליצירת קשר.]</p>
        
        <h3>📧 [translate:הגדרת קמפיין]</h3>
        
        <div class="substep">
            <h4>[translate:יצירת קמפיין]</h4>
            <p>[translate:צור קמפיין חדש ב-LaGrowthMachine וייבא את הלידים המכושרים שלך מ-Clay. הגדר את פרמטרי הקמפיין הבסיסיים והגדרות המיקוד.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 51 17.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הגדרת רצף הודעות]</h4>
            <p>[translate:הגדר את רצף הודעות יצירת הקשר שלך, כולל בקשות חיבור ראשוניות, הודעות מעקב ומשתני פרסונליזציה. השתמש בנתונים מ-Clay כדי לפרסן כל נקודת מגע.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 51 41.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 51 51.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הגדרות זמן ותדירות]</h4>
            <p>[translate:הגדר זמון אופטימלי לפעילויות יצירת הקשר שלך. הגדר עיכובים בין הודעות, מגבלות שליחה יומיות ושיקולי אזור זמן לאפקטיביות מקסימלית.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 52 02.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 52 07.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:פרסונליזציה ומשתנים]</h4>
            <p>[translate:יישם פרסונליזציה דינמית באמצעות הנתונים המועשרים מ-Clay. הגדר משתנים לשמות, חברות, תפקידים ומידע ספציפי לתעשייה.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 54 43.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 54 44.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:הגדרת ניטור קמפיין]</h4>
            <p>[translate:הגדר מעקב וניטור לביצועי הקמפיין שלך. הגדר אנליטיקה, מעקב תגובות וניטור המרות כדי למדוד הצלחה.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 55 27.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:סקירה סופית של הקמפיין]</h4>
            <p>[translate:סקור את כל הגדרות הקמפיין, בדוק רצפי הודעות ואמת שכל האינטגרציות עובדות כראוי לפני השקת האוטומציה שלך.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 56 48.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 57 10.png]
            </div>
        </div>
        
        <div class="substep">
            <h4>[translate:השקת קמפיין]</h4>
            <p>[translate:השק את קמפיין יצירת הקשר האוטומטי שלך בלינקדאין ועקוב אחר הביצועים הראשוניים. הגדר בדיקות רגילות כדי לייעל ביצועי הודעות ושיעורי תגובה.]</p>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 57 20.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 58 19.png]
            </div>
            <div class="image-placeholder">
                [INSERT IMAGE: 5_lgm_setup_campaign/2025-09-15 16 58 28.png]
            </div>
        </div>
        
        <div class="success">
            <strong>[translate:קמפיין פעיל:]</strong> [translate:צינור האוטומציה שלך בלינקדאין כעת חי ופועל! עקוב אחר הביצועים ויעל בהתבסס על נתוני תגובה.]
        </div>
    </div>
</section>

<!-- Best Practices Section -->
<section class="step-section">
    <div class="step-header">
        <h2><span class="step-number">💡</span>[translate:שיטות עבודה מומלצות וטיפים לייעול]</h2>
    </div>
    <div class="step-content">
        <h3>🎯 [translate:ייעול קמפיין]</h3>
        <ul>
            <li><strong>[translate:בדיקת A/B להודעות:]</strong> [translate:בדוק ללא הרף וריאציות שונות של הודעות כדי לשפר שיעורי תגובה]</li>
            <li><strong>[translate:ניטור מגבלות לינקדאין:]</strong> [translate:הישאר בגבולות מגבלות החיבור וההודעות היומיות של לינקדאין כדי למנוע הגבלות חשבון]</li>
            <li><strong>[translate:איכות פרסונליזציה:]</strong> [translate:השתמש בהעשרת הנתונים של Clay כדי ליצור הודעות יצירת קשר מותאמות אישית ורלוונטיות]</li>
            <li><strong>[translate:ניהול תגובות:]</strong> [translate:הגדר מערכות לטיפול בתגובות ופרוספקטים מעוניינים במהירות ובמקצועיות]</li>
        </ul>
        
        <h3>📊 [translate:ניטור ביצועים]</h3>
        <ul>
            <li><strong>[translate:מדדים מרכזיים:]</strong> [translate:עקוב אחר שיעורי קבלת חיבורים, שיעורי תגובה והמרה לפגישות]</li>
            <li><strong>[translate:איכות נתונים:]</strong> [translate:בדוק באופן קבוע את זרימות העבודה של Clay כדי להבטיח שאיכות הלידים נשארת גבוהה]</li>
            <li><strong>[translate:אנליטיקת קמפיינים:]</strong> [translate:השתמש באנליטיקה המובנית של LGM כדי לזהות רצפי הודעות בעלי הביצועים הטובים ביותר]</li>
            <li><strong>[translate:מעקב ROI:]</strong> [translate:מדוד את ההשפעה העסקית של מאמצי האוטומציה שלך]</li>
        </ul>
        
        <div class="warning">
            <strong>[translate:הערת תאימות:]</strong> [translate:תמיד עמוד בתנאי השירות של לינקדאין ובתקנות הגנת נתונים רלוונטיות (GDPR, CCPA) כאשר מבצע יצירת קשר אוטומטית.]
        </div>
    </div>
</section>

<div class="footer">
    <h3>🎉 [translate:ברכות!]</h3>
    <p>[translate:הגדרת בהצלחה צינור אוטומציה מקיף בלינקדאין המשלב ייצור לידים חכם עם אוטומציית יצירת קשר מותאמת אישית.]</p>
    <p><strong>[translate:רכיבי הצינור:]</strong> [translate:מודיעין לידים של Clay.com + אוטומציה של LaGrowthMachine = יצירת קשר בלינקדאין ניתנת להרחבה]</p>
</div>

</body>
</html>

