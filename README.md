# Cleaning the text and converting it into a basic HTML structure
import re

# Define HTML template
html_template = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CV - Mohamed Tayel</title>
    <style>
        body {{
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }}
        h1, h2, h3 {{
            color: #2E86C1;
        }}
        .contact {{
            font-size: 1.2em;
        }}
        .section {{
            margin-bottom: 20px;
        }}
        ul {{
            list-style-type: none;
            padding: 0;
        }}
        ul li {{
            margin: 5px 0;
        }}
    </style>
</head>
<body>

<h1>MOHAMED TAYEL</h1>
<h2>Offshore Company Site Representative & Offshore Installation Manager</h2>

<div class="contact">
    <p><strong>Nationality:</strong> Egyptian</p>
    <p><strong>Date of Birth:</strong> 23rd Nov, 1980</p>
    <p><strong>Marital Status:</strong> Married</p>
    <p><strong>Email:</strong> Moh.tayel@gmail.com</p>
    <p><strong>Phone:</strong> +44 7458 938902 & +34 87797 1003</p>
    <p><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/mohamed-tayel-a0889019/">linkedin.com/in/mohamed-tayel</a></p>
</div>

<div class="section">
    <h2>Professional Summary</h2>
    <p>A Highly adaptable senior Project Engineer & offshore installation manager, accredited as a Marine Warranty surveyor with over 21 years of extensive experience in onshore/offshore installation, top-side and subsea construction, and IRM activities...</p>
</div>

<div class="section">
    <h2>Skills</h2>
    <ul>
        <li>Operations & Project Management</li>
        <li>Over 20 years experience in offshore marine installation</li>
        <li>Engineering, Planning, and Logistics support for offshore installation work</li>
        <li>Developing and reviewing detailed offshore installation procedures</li>
        <!-- More Skills -->
    </ul>
</div>

<div class="section">
    <h2>University Degree</h2>
    <ul>
        <li>B.Sc. Mechanical Engineering, Alex. University, June 2003</li>
        <li>MBA in Project Management, Charisma University, UK, Dec. 2019</li>
    </ul>
</div>

<div class="section">

# Continuing the HTML structure process after extracting text and planning to clean and convert it.

# HTML template initialization
html_template = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohamed Tayel CV</title>
    <style>
        body {{
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }}
        h1, h2 {{
            color: #003366;
        }}
        .section {{
            margin-bottom: 20px;
        }}
        .section-title {{
            font-size: 1.5em;
            font-weight: bold;
            border-bottom: 2px solid #003366;
            padding-bottom: 5px;
        }}
        .personal-info, .skills, .experience {{
            margin-top: 10px;
        }}
        ul {{
            margin: 0;
            padding: 0;
            list-style-type: none;
        }}
        ul li {{
            margin-bottom: 5px;
        }}
        .contact {{
            margin-top: 10px;
            font-size: 0.9em;
        }}
        .contact a {{
            color: #003366;
            text-decoration: none;
        }}
        .contact a:hover {{
            text-decoration: underline;
        }}
    </style>
</head>
<body>
    <h1>MOHAMED TAYEL</h1>
    <p>Offshore Company Site Representative & Offshore Installation Manager & PMC, Lead Project Engineer</p>

    <div class="personal-info">
        <p><strong>Nationality:</strong> Egyptian</p>
        <p><strong>Date of Birth:</strong> 23rd Nov, 1980</p>
        <p><strong>Marital Status:</strong> Married</p>
        <p><strong>Email:</strong> <a href="mailto:moh.tayel@gmail.com">moh.tayel@gmail.com</a></p>
        <p><strong>Telephones:</strong> +44 7458 938902 &amp; +34 87797 1003</p>
        <p><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/mohamed-tayel-a0889019/">Mohamed Tayel</a></p>
    </div>

    <div class="section">
        <h2 class="section-title">Professional Summary</h2>
        <p>A highly adaptable senior Project Engineer & offshore installation manager with 21+ years of experience in offshore and onshore projects, subsea construction, IRM activities, and deep/shallow water operations. Accredited Marine Warranty Surveyor with extensive management skills and a proven ability to oversee complex projects and diverse teams.</p>
    </div>

    <div class="section">
        <h2 class="section-title">Career Accomplishments</h2>
        <ul>
            <li>Extensive experience in managing offshore installations and projects across various regions.</li>
            <li>Proven ability to resolve client issues and maintain relationships with key stakeholders.</li>
            <li>Closed multi-million-dollar contracts with major oil and gas companies.</li>
            <li>Led cross-functional teams and ensured safety and regulatory compliance in offshore operations.</li>
        </ul>
    </div>

    <div class="section">
        <h2 class="section-title">Skills</h2>
        <ul>
            <li>Operations & Project Manager for Marine, Diving, ROV & Survey</li>
            <li>20+ years in offshore installation, platform construction, pipeline installation</li>
            <li>Engineering and logistics for offshore projects</li>
            <li>Audits for diving and marine systems (IMCA Standards)</li>
        </ul>
    </div>

    <div class="section">
        <h2 class="section-title">Qualifications</h2>
        <ul>
            <li>B.Sc. in Mechanical Engineering, Alexandria University (2003)</li>
            <li>MBA in Project Management, Charisma University, UK (2019)</li>
            <li>Accredited Marine Warranty Surveyor, Lloyd Maritime Institute, London (2021)</li>
            <li>CSWIP 3.4u Underwater Inspection Controller</li>
            <li>NEBOSH Certificate, IOSH Managing Safely Certificate</li>
        </ul>
    </div>

    <div class="section">
        <h2 class="section-title">Languages</h2>
        <ul>
            <li>Arabic: Mother tongue</li>
            <li>English: Fluent (Read, Written, Spoken)</li>
            <li>Spanish: Adequate knowledge, progressing to intermediate</li>
            <li>Italian: Adequate knowledge, progressing to intermediate</li>
            <li>Portuguese: Beginner Level</li>
        </ul>
    </div>

    <div class="section">
        <h2 class="section-title">Professional Experience</h2>
        <h3>ENI CONGO / ENI IVORY COAST, 2021 – Present</h3>
        <p><strong>Role:</strong> Offshore Company Site Representative</p>
        <ul>
            <li>Managed offshore installations in deep and shallow water.</li>
            <li>Oversaw complex installation campaigns (e.g., mooring lines, flexible risers, spools).</li>
            <li>Ensured project delivery within safety, time, and budget constraints.</li>
        </ul>

        <h3>SEA HORSE OILFIELD SERVICES, 2021</h3>
        <p><strong>Role:</strong> Project Manager</p>
        <ul>
            <li>Led offshore pipeline replacement projects.</li>
            <li>Responsible for project execution and marine spread selection.</li>
        </ul>
        <!-- Additional experiences would follow in the same pattern -->
    </div>

    <div class="contact">
        <h2>References</h2>
        <ul>
            <li>David Croce - Offshore Installation Manager – ENI Côte d’Ivoire (david.croce@eni.com)</li>
            <li>Ronet Okombi – Technical Director - ENI Congo (ronet.okombi-yombi@eni.com)</li>
            <!-- Additional references here -->
        </ul>
    </div>
</body>
</html>
"""

# Save to an HTML file for the user
html_output_path = '/mnt/data/Mohamed_Tayel_CV.html'
with open(html_output_path, 'w') as f:
    f.write(html_template)

html_output_path

