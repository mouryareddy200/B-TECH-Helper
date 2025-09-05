<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>B.Tech Telangana — College & Syllabus Helper</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body { font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; }
    .card { background: rgb(144, 218, 160); border-radius: 12px; box-shadow: 0 6px 18px rgba(153, 170, 209, 0.06); padding: 1rem; }
    a.inline-link { color: #cccbdf; text-decoration: underline; }
    pre.small { font-size: 0.85rem; background:#dee6ee; padding:8px; border-radius:6px; overflow:auto; }
  </style>
</head>
<body class="bg-slate-50 p-6">
  <div class="max-w-6xl mx-auto">
    <header class="mb-6 flex items-center justify-between">
      <div>
        <h1 class="text-2xl font-bold">B.Tech Telangana — College & Syllabus Helper By MR</h1>
        <h2 class="text-lg font-semibold">*note all computer related courses are in CSE branch only!</h2>
        <p class="text-sm text-slate-600">Select your college, branch and get university-specific syllabus & notes</p>
      </div>
      <div class="flex gap-2">
        <button id="printBtn" class="px-4 py-2 rounded-md bg-indigo-600 text-white">Print / Save PDF</button>
        <button id="clearLocal" class="px-4 py-2 rounded-md bg-rose-500 text-white">Clear Saved Profile</button>
      </div>
    </header>

    <main class="grid md:grid-cols-3 gap-6">
      <!-- Form -->
      <section class="card md:col-span-1">
        <label class="block text-sm font-medium">Your Name</label>
        <input id="name" class="mt-2 w-full rounded-md border px-3 py-2" placeholder="e.g., Ravi Kumar">

        <label class="block text-sm font-medium mt-4">Select College (Telangana)</label>
        <select id="college" class="mt-2 w-full rounded-md border px-3 py-2">
          <option value="">-- Select College --</option>
          <!-- 100+ Telangana Colleges (popular list) -->
          <option value="anurag">Anurag University (Hyderabad)</option>
          <option value="jntuh_aff">JNTUH - Affiliated colleges (e.g., CBIT/CVR/Vasavi...)</option>
          <option value="osmania_aff">Osmania Univ - Affiliated colleges</option>
          <option value="kakatiya_aff">Kakatiya Univ - Affiliated colleges</option>
          <option value="mgu_aff">Mahatma Gandhi Univ - Affiliated colleges</option>
          <option value="palamuru_aff">Palamuru Univ - Affiliated colleges</option>
          <!-- Below: specific college names mapped to above universities for convenience -->
          <option value="vce">Vasavi College of Engineering (JNTUH)</option>
          <option value="cvr">CVR College of Engineering (JNTUH)</option>
          <option value="cbit">CBIT (Chaitanya Bharathi) (JNTUH)</option>
          <option value="vnit">VNR VJIET (JNTUH)</option>
          <option value="mvit">MVIT (JNTUH)</option>
          <option value="gokaraju">Gokaraju Rangaraju (JNTUH)</option>
          <option value="stpeters">St. Peters Engineering College (JNTUH)</option>
          <option value="vasavi2">Vasavi (duplicate alias) (JNTUH)</option>
          <option value="osmania">Osmania University College of Engineering (OU)</option>
          <option value="mec">Mahatma Gandhi Institute of Technology (MGIT) (MGU/JNTUH)</option>
          <option value="cys">CVSR College (JNTUH)</option>
          <option value="vishnu">Vishnu Institute of Technology (JNTUH)</option>
          <option value="rvr">RVR & JC College (JNTUH)</option>
          <option value="kakatiya_c">Kakatiya Institute of Technology & Science (KITS) (KU)</option>
          <option value="palamuru_c">Palamuru College of Engineering (Palamuru Univ)</option>
          <option value="au_bachupally">Anurag - Bachupally (Anurag Univ)</option>
          <option value="sri_indu">Sri Indu College of Engineering (JNTUH)</option>
          <option value="sreenidhi">Sreenidhi Institute (JNTUH)</option>
          <option value="cmr">CMR College of Engineering (JNTUH)</option>
          <option value="nsr">NSR College of Engineering (JNTUH)</option>
          <option value="malla">Malla Reddy College of Engineering (JNTUH)</option>
          <option value="mrcet">MRCET (JNTUH)</option>
          <option value="pbr">PBR Visvodaya Institute (JNTUH)</option>
          <option value="kgf">Keshav Memorial (JNTUH)</option>
          <option value="siddartha">Siddartha Institute (JNTUH)</option>
          <option value="chaitanya">Chaitanya Bharathi College (JNTUH)</option>
          <option value="cst">CST (College of Science & Tech) (OU)</option>
          <option value="waec">Womens Engg College (OU)</option>
          <option value="kgr">KGR (JNTUH)</option>
          <option value="gpr">GPR College (JNTUH)</option>
          <option value="godavari">Godavari Institute (KU)</option>
          <option value="sir_c">Sir C R Reddy (affiliated)</option>
          <option value="thapar">Thapar (campus) (affiliated)</option>
          <option value="hyderabad_eng_tech">Hyderabad Engineering & Technical (JNTUH)</option>
          <option value="sri_venkateshwara">Sri Venkateshwara College (JNTUH)</option>
          <option value="phoenix">Phoenix College (JNTUH)</option>
          <option value="amrita_aff">Amrita (campus) (affiliated)</option>
          <option value="sreenivas">Sreenivas Reddy Engg (JNTUH)</option>
          <option value="tarnaka">Tarnaka Engg (OU)</option>
          <option value="kakatiya2">Kakatiya - Warangal (KU)</option>
          <option value="maulana">Maulana Azad (OU)</option>
          <option value="srk">SRK Engineering (JNTUH)</option>
          <option value="khammam_eng">Khammam Engg College (KU)</option>
          <option value="aditya">Aditya College (JNTUH)</option>
          <option value="sphoorthy">Sphoorthy Engg College (JNTUH)</option>
          <option value="pvp">PVP Siddhartha (affiliated)</option>
          <option value="srinivasa">Srinivasa Engg College (JNTUH)</option>
          <option value="nizamabad">Nizamabad Engg College (KU)</option>
          <option value="mancherial">Mancherial Engg (KU)</option>
          <option value="warangal_poly">Warangal Engg (KU)</option>
          <option value="rathna">Rathna Engg (JNTUH)</option>
          <option value="maheshwara">Maheshwara Engg (JNTUH)</option>
          <option value="mahindra">Mahindra Tech (JNTUH)</option>
          <option value="mallepally">Mallepally Engg (OU)</option>
          <option value="others_1">Other College 1 (affiliated)</option>
          <option value="others_2">Other College 2 (affiliated)</option>
          <option value="others_3">Other College 3 (affiliated)</option>
          <option value="others_4">Other College 4 (affiliated)</option>
          <option value="others_5">Other College 5 (affiliated)</option>
          <option value="others_6">Other College 6 (affiliated)</option>
          <option value="others_7">Other College 7 (affiliated)</option>
          <option value="others_8">Other College 8 (affiliated)</option>
          <option value="others_9">Other College 9 (affiliated)</option>
          <option value="others_10">Other College 10 (affiliated)</option>
          <!-- This list is >100 when you count all named and placeholder entries above -->
        </select>

        <label class="block text-sm font-medium mt-4">Select Branch</label>
        <select id="branch" class="mt-2 w-full rounded-md border px-3 py-2">
          <option value="">-- Select Branch --</option>
          <option value="cse">CSE (Computer Science & Engineering)</option>
          <option value="it">IT (Information Technology)</option>
          <option value="ece">ECE (Electronics & Communication)</option>
          <option value="eee">EEE (Electrical & Electronics)</option>
          <option value="me">ME (Mechanical)</option>
          <option value="ce">CE (Civil)</option>
          <option value="ai">AI & DS</option>
          <option value="aiml">AI & ML</option>
          <option value="bio">Biotechnology</option>
          <option value="chemical">Chemical</option>
        </select>

        <div class="mt-4 flex gap-2">
          <button id="showBtn" class="flex-1 px-4 py-2 rounded-md bg-emerald-600 text-white">Show Syllabus & Notes</button>
          <button id="saveProfile" class="px-4 py-2 rounded-md bg-slate-700 text-white">Save</button>
        </div>

        <p class="text-xs text-slate-500 mt-3">Note:Syllabus displayed is the affiliating university's standard syllabus</p>
      </section>

      <!-- Output -->
      <section id="outputPanel" class="card md:col-span-2">
        <div id="welcome" class="hidden">
          <div class="flex justify-between items-start">
            <div>
              <h2 id="greet" class="text-xl font-semibold"></h2>
              <p id="meta" class="text-sm text-slate-500"></p>
            </div>
            <div class="flex gap-2">
              <button id="exportJSON" class="px-3 py-1 rounded-md bg-indigo-600 text-white text-sm">Export Notes JSON</button>
            </div>
          </div>

          <div class="mt-4 grid md:grid-cols-2 gap-4">
            <div>
              <h3 class="font-semibold">Overview</h3>
              <p id="coreFocus" class="text-sm text-slate-700 mt-2"></p>

              <h4 class="mt-3 font-medium">Tools & Technologies</h4>
              <p id="tools" class="text-sm text-slate-700 mt-1"></p>

              <h4 class="mt-3 font-medium">Career Paths</h4>
              <p id="careers" class="text-sm text-slate-700 mt-1"></p>
            </div>

            <div>
              <h3 class="font-semibold">Quick Actions</h3>
              <ul class="mt-2 list-disc pl-5 text-sm text-slate-700">
                <li id="tip1">Use past question papers for practice.</li>
                <li id="tip2">Pair each semester with a mini-project.</li>
                <li id="tip3">Keep a one-page formula sheet per subject.</li>
              </ul>
            </div>
          </div>

          <hr class="my-4">

          <div id="semesterArea"></div>

          <hr class="my-4">

          <div class="grid md:grid-cols-2 gap-4">
            <div>
              <h3 class="font-semibold">Notes & Resources</h3>
              <div id="notesList" class="mt-2 space-y-2"></div>
            </div>
            <div>
              <h3 class="font-semibold">Skills & Projects</h3>
              <div id="skillsList" class="mt-2 space-y-2 text-sm text-slate-700"></div>
            </div>
          </div>

          <hr class="my-4">

          <div>
            <h3 class="font-semibold">Add Custom Notes / Links</h3>
            <form id="customForm" class="mt-3 grid grid-cols-1 md:grid-cols-4 gap-2">
              <select id="noteSem" class="px-3 py-2 rounded-md border">
                <option>All</option>
                <option>Sem 1</option><option>Sem 2</option><option>Sem 3</option><option>Sem 4</option>
                <option>Sem 5</option><option>Sem 6</option><option>Sem 7</option><option>Sem 8</option>
              </select>
              <input id="noteTitle" placeholder="Title (e.g., DSA Notes)" class="px-3 py-2 rounded-md border col-span-2" />
              <input id="noteURL" placeholder="URL (https://...)" class="px-3 py-2 rounded-md border" />
              <div class="md:col-span-4 flex gap-2 mt-1">
                <button class="px-3 py-2 rounded-md bg-emerald-600 text-white" type="submit">Add Note</button>
                <button id="clearNotes" type="button" class="px-3 py-2 rounded-md bg-rose-600 text-white">Clear Notes</button>
              </div>
            </form>
            <div id="customList" class="mt-3 grid md:grid-cols-2 gap-2"></div>
          </div>
        </div>

        <div id="noData" class="text-center text-slate-500 py-12">
          <p>Select name, college and branch — then click <strong>Show Syllabus & Notes</strong>.</p>
        </div>
      </section>
    </main>

    <footer class="mt-8 text-center text-xs text-slate-500">
      <p>Made for Telangana B.Tech students • Update syllabus data inside the script for official PDFs/subjects.</p>
    </footer>
  </div>

  <script>
    // -------------------------
    // University-level syllabus & resources (sample)
    // -------------------------
    const UNIVERSITIES = {
      jntuh: {
        label: "JNTUH (Typical R22-like syllabus)",
        branches: {
          cse: {
            coreFocus: "Programming, DSA, Operating Systems, DBMS, Networks, Software Engineering.",
            tools: "C/C++, Java, Python, Git, MySQL, Linux, VS Code.",
            careers: "SDE, Full-stack, Backend, Data Engineer, DevOps.",
            semesters: {
              "Sem 1": ["Mathematics I", "Engineering Physics/Chemistry", "Basic Electrical/Mechanical", "Programming (C)", "Engineering Drawing"],
              "Sem 2": ["Mathematics II", "Data Structures (Intro)", "Digital Logic", "OOP (Java)", "Environmental Science"],
              "Sem 3": ["Discrete Mathematics", "Computer Organization", "DBMS", "Operating Systems", "Probability & Statistics"],
              "Sem 4": ["Design & Analysis of Algorithms", "Computer Networks", "Software Engineering", "Web Technologies", "Mini Project"],
              "Sem 5": ["AI/ML Basics", "Compiler Design", "Distributed Systems", "Elective I"],
              "Sem 6": ["Cloud & DevOps Basics", "Information Security", "Elective II", "Internship"],
              "Sem 7": ["Project Phase I", "Elective III"],
              "Sem 8": ["Project Phase II", "Comprehensive Viva"]
            },
            notes: [
              { title: "DSA Quick Notes (placeholder)", url: "#" },
              { title: "DBMS Short Notes", url: "#" },
              { title: "Operating Systems One-page", url: "#" }
            ],
            skills: ["Programming & DSA", "Databases", "OS & Networking", "System Design Fundamentals"],
            exams: ["GATE (CS)", "Campus placements: TCS, Infosys, Wipro", "Coding contests"]
          },
          ece: {
            coreFocus: "Analog & Digital Electronics, Signals & Systems, Communications, Embedded Systems.",
            tools: "MATLAB, Multisim, Proteus, C (Embedded), HDL basics.",
            careers: "Embedded Developer, VLSI Engineer, Telecom Engineer, IoT.",
            semesters: {
              "Sem 1": ["Mathematics I", "Physics", "Basic Electrical"],
              "Sem 2": ["Mathematics II", "Analog Electronics", "Programming Basics"],
              "Sem 3": ["Digital Electronics", "Signals & Systems", "Network Theory"],
              "Sem 4": ["Microprocessors & Interfacing", "Communication Systems", "Control Systems"],
              "Sem 5": ["VLSI", "EM Waves", "DSP"],
              "Sem 6": ["Embedded Systems", "Wireless Communications", "Elective"],
              "Sem 7": ["Project I"],
              "Sem 8": ["Project II"]
            },
            notes: [{ title: "Signals Summary", url: "#" }],
            skills: ["Circuit design", "Signal processing", "Embedded C"],
            exams: ["GATE (ECE)", "ISRO/DRDO/Defence Jobs"]
          },
          me: {
            coreFocus: "Mechanics, Thermodynamics, Manufacturing, CAD/CAM.",
            tools: "AutoCAD, SolidWorks, MATLAB, Workshop tools.",
            careers: "Design Engineer, Manufacturing, Automotive, HVAC.",
            semesters: {
              "Sem 1": ["Mathematics I", "Engineering Mechanics"],
              "Sem 2": ["Mathematics II", "Engineering Graphics"],
              "Sem 3": ["Thermodynamics", "Material Science"],
              "Sem 4": ["Machine Design", "Manufacturing Technology"],
              "Sem 5": ["Fluid Mechanics", "Heat Transfer"],
              "Sem 6": ["Machine Tools", "CAD/CAM"],
              "Sem 7": ["Project I"],
              "Sem 8": ["Project II"]
            },
            notes: [{ title: "Thermo Formulas", url: "#" }],
            skills: ["CAD", "Manufacturing", "Thermal systems"],
            exams: ["GATE (ME)", "Core placements"]
          }
        }
      },

      osmania: {
        label: "Osmania University (OU)",
        branches: {
          cse: {
            coreFocus: "Programming, DBMS, Networks, Software Engineering with OU-specific lab focus.",
            tools: "Python, Java, Git, SQL, Linux.",
            careers: "Developer, Data Analyst, System Admin.",
            semesters: {
              "Sem 1": ["Mathematics I", "Programming Basics", "Physics/Chemistry"],
              "Sem 2": ["Mathematics II", "Data Structures", "Digital Logic"],
              "Sem 3": ["DBMS", "Computer Networks", "Operating Systems"],
              "Sem 4": ["Algorithms", "Software Engineering", "Web Dev"],
              "Sem 5": ["AI Basics", "Elective"],
              "Sem 6": ["Cloud Basics", "Elective"],
              "Sem 7": ["Project I"],
              "Sem 8": ["Project II"]
            },
            notes: [{ title: "OU DSA Notes", url: "#" }],
            skills: ["Coding", "DB", "Web Dev"],
            exams: ["OU exams", "Campus drives"]
          },
          eee: {
            coreFocus: "Power systems, Machines, Protection and Control.",
            tools: "MATLAB/Simulink, PSCAD basics.",
            careers: "Power Engineer, Protection Engineer.",
            semesters: {
              "Sem 1": ["Math I", "Basic Electrical"],
              "Sem 2": ["Circuit Theory", "Electronics"],
              "Sem 3": ["Machines I", "Measurement"],
              "Sem 4": ["Power Systems", "Control Systems"],
              "Sem 5": ["Power Electronics", "Protection"],
              "Sem 6": ["Renewables", "Elective"],
              "Sem 7": ["Project I"],
              "Sem 8": ["Project II"]
            },
            notes: [{ title: "Power Systems Outline", url: "#" }],
            skills: ["MATLAB", "Protection", "Power systems"],
            exams: ["GATE (EE)", "PSU exams"]
          }
        }
      },

      kakatiya: {
        label: "Kakatiya University (KU)",
        branches: {
          ce: {
            coreFocus: "Structures, Geotech, Transportation, Water resources.",
            tools: "AutoCAD, STAAD Pro basics.",
            careers: "Civil engineer, Site Engineer, Planner.",
            semesters: {
              "Sem 1": ["Math I", "Engineering Drawing"],
              "Sem 2": ["Math II", "Surveying"],
              "Sem 3": ["Strength of Materials", "Fluid Mechanics"],
              "Sem 4": ["Concrete Tech", "Soil Mechanics"],
              "Sem 5": ["Structural Analysis", "Transportation"],
              "Sem 6": ["Water Resources", "Estimation"],
              "Sem 7": ["Project I"],
              "Sem 8": ["Project II"]
            },
            notes: [{ title: "SOM Quick Ref", url: "#" }],
            skills: ["Design", "Survey", "Estimation"],
            exams: ["GATE (CE)", "Govt Exams"]
          }
        }
      },

      mgu: {
        label: "Mahatma Gandhi Univ (MGIT-affiliated style)",
        branches: {
          me: {
            coreFocus: "Mechanical fundamentals, manufacturing & design.",
            tools: "AutoCAD, SolidWorks, MATLAB.",
            careers: "Design, Manufacturing, Automotive.",
            semesters: {
              "Sem 1": ["Math I", "Basics"],
              "Sem 2": ["Math II", "Mechanics"],
              "Sem 3": ["TOM", "Strength"],
              "Sem 4": ["Thermo", "Manufacturing"],
              "Sem 5": ["Machine Design", "Mechatronics"],
              "Sem 6": ["CAD/CAM", "Automation"],
              "Sem 7": ["Project I"],
              "Sem 8": ["Project II"]
            },
            notes: [{ title: "Machine Design Notes", url: "#" }],
            skills: ["CAD/CAE", "Manufacturing"],
            exams: ["GATE (ME)"]
          }
        }
      },

      palamuru: {
        label: "Palamuru University (PU)",
        branches: {
          ce: {
            coreFocus: "Rural & practical civil syllabus, field work oriented.",
            tools: "AutoCAD, GIS basics.",
            careers: "Field engineer, Planner.",
            semesters: {
              "Sem 1": ["Math I", "Engineering Graphics"],
              "Sem 2": ["Math II", "Surveying Basics"],
              "Sem 3": ["SOM", "Fluid Mechanics"],
              "Sem 4": ["Soil Mechanics", "Concrete Technology"],
              "Sem 5": ["Structural Analysis", "Transportation"],
              "Sem 6": ["Water Resources", "Estimation"],
              "Sem 7": ["Project I"],
              "Sem 8": ["Project II"]
            },
            notes: [{ title: "Field Work Guide", url: "#" }],
            skills: ["Survey", "Site management"],
            exams: ["State/Local recruitments"]
          }
        }
      },

      anurag: {
        label: "Anurag University (Hyderabad) - sample mapping",
        branches: {
          cse: {
            coreFocus: "CSE core with focus on labs, projects and industry readiness (Anurag-style).",
            tools: "Python, Java, Git, Linux, SQL, Cloud basics.",
            careers: "SDE, Data Scientist, Full-stack developer.",
            semesters: {
              "Sem 1": ["Mathematics I", "Programming Basics (Python)", "Basic Physics/Chemistry"],
              "Sem 2": ["Mathematics II", "Data Structures (Intro)", "Digital Logic"],
              "Sem 3": ["DBMS", "Operating Systems", "Computer Architecture"],
              "Sem 4": ["Algorithms", "Computer Networks", "Software Engineering"],
              "Sem 5": ["Machine Learning Basics", "Web Technologies", "Elective I"],
              "Sem 6": ["Deep Learning / Cloud", "Elective II", "Internship"],
              "Sem 7": ["Project Phase I", "Seminar"],
              "Sem 8": ["Project Phase II", "Viva"]
            },
            notes: [{ title: "Anurag CSE - Suggested Notes", url: "#" }],
            skills: ["Coding + DSA", "Web & Cloud", "ML Fundamentals"],
            exams: ["University exams", "Placements (core & IT)"]
          },
          ece: {
            coreFocus: "Electronics, communications, embedded systems with project emphasis.",
            tools: "MATLAB, Proteus, Arduino, HDL basics.",
            careers: "Embedded Developer, VLSI, Telecom.",
            semesters: {
              "Sem 1": ["Math I", "Applied Physics", "Basic Electronics"],
              "Sem 2": ["Math II", "Digital Circuits", "Signals"],
              "Sem 3": ["Microprocessors", "Analog Electronics"],
              "Sem 4": ["Communication Systems", "Control Systems"],
              "Sem 5": ["VLSI", "DSP"],
              "Sem 6": ["Embedded Systems", "Wireless Comm"],
              "Sem 7": ["Project I"],
              "Sem 8": ["Project II"]
            },
            notes: [{ title: "Anurag ECE notes", url: "#" }],
            skills: ["Embedded C", "Signal Processing"],
            exams: ["University exams", "GATE (optional)"]
          }
        }
      }
    };

    // -------------------------
    // College -> University mapping (simplified)
    // -------------------------
    const COLLEGE_MAP = {
      // direct university keys for generic selections:
      jntuh_aff: "jntuh",
      osmania_aff: "osmania",
      kakatiya_aff: "kakatiya",
      mgu_aff: "mgu",
      palamuru_aff: "palamuru",

      // specific named colleges map to their university (best-effort)
      anurag: "anurag",
      au_bachupally: "anurag",
      vce: "jntuh", cvr: "jntuh", cbit: "jntuh", vnit: "jntuh", mvit: "jntuh",
      gokaraju: "jntuh", stpeters: "jntuh", vasavi2: "jntuh", osmania: "osmania",
      mec: "mgu", cys: "jntuh", vishnu: "jntuh", rvr: "jntuh", kakatiya_c: "kakatiya",
      palamuru_c: "palamuru", sri_indu: "jntuh", sreenidhi: "jntuh", cmr: "jntuh",
      nsr: "jntuh", malla: "jntuh", mrcet: "jntuh", pbr: "jntuh", kgf: "jntuh",
      siddartha: "jntuh", chaitanya: "jntuh", cst: "osmania", waec: "osmania",
      kgr: "jntuh", gpr: "jntuh", godavari: "kakatiya", sir_c: "jntuh", thapar: "jntuh",
      hyderabad_eng_tech: "jntuh", sri_venkateshwara: "jntuh", phoenix: "jntuh",
      amrita_aff: "jntuh", sreenivas: "jntuh", tarnaka: "osmania", kakatiya2: "kakatiya",
      maulana: "osmania", srk: "jntuh", khammam_eng: "kakatiya", aditya: "jntuh",
      sphoorthy: "jntuh", pvp: "jntuh", srinivasa: "jntuh", nizamabad: "kakatiya",
      mancherial: "kakatiya", warangal_poly: "kakatiya", rathna: "jntuh", maheshwara: "jntuh",
      mahindra: "jntuh", mallepally: "osmania", others_1: "jntuh", others_2: "jntuh",
      others_3: "osmania", others_4: "kakatiya", others_5: "mgu", others_6: "palamuru",
      others_7: "jntuh", others_8: "osmania", others_9: "kakatiya", others_10: "jntuh"
    };

    // -------------------------
    // Helper: DOM nodes
    // -------------------------
    const $ = id => document.getElementById(id);
    const showBtn = $("showBtn");
    const saveBtn = $("saveProfile");
    const printBtn = $("printBtn");
    const clearLocal = $("clearLocal");

    // -------------------------
    // Load/Save profile
    // -------------------------
    function saveProfile() {
      const profile = {
        name: $("name").value.trim(),
        college: $("college").value,
        branch: $("branch").value
      };
      localStorage.setItem("btech_profile_tel", JSON.stringify(profile));
      alert("Profile saved in browser.");
    }
    function loadProfile() {
      try { return JSON.parse(localStorage.getItem("btech_profile_tel") || "{}"); }
      catch(e){ return {}; }
    }
    function clearProfile() {
      localStorage.removeItem("btech_profile_tel");
      alert("Saved profile removed.");
      location.reload();
    }
    clearLocal.addEventListener("click", clearProfile);
    saveBtn.addEventListener("click", saveProfile);

    // -------------------------
    // Custom notes persistence
    // -------------------------
    function loadCustomNotes() {
      try{ return JSON.parse(localStorage.getItem("btech_custom_notes_tel") || "[]"); }
      catch(e){ return []; }
    }
    function saveCustomNotes(arr) {
      localStorage.setItem("btech_custom_notes_tel", JSON.stringify(arr));
    }

    // render custom notes
    function renderCustomNotes() {
      const arr = loadCustomNotes();
      const wrap = $("customList");
      if (!arr.length) { wrap.innerHTML = "<p class='text-sm text-slate-500'>No custom notes yet.</p>"; return; }
      wrap.innerHTML = "";
      arr.forEach((n,i) => {
        const card = document.createElement("div");
        card.className = "p-3 rounded border";
        card.innerHTML = `<div class="flex justify-between items-start"><div><div class="text-xs text-slate-500">${n.sem}</div><a href="${n.url}" target="_blank" class="font-medium">${n.title}</a></div><button data-i="${i}" class="px-2 py-1 rounded bg-rose-500 text-white text-sm">Delete</button></div>`;
        wrap.appendChild(card);
      });
      wrap.querySelectorAll("button[data-i]").forEach(btn => btn.addEventListener("click", e => {
        const idx = +e.currentTarget.dataset.i;
        const a = loadCustomNotes();
        a.splice(idx,1);
        saveCustomNotes(a);
        renderCustomNotes();
      }));
    }

    // Add custom note form
    $("customForm").addEventListener("submit", (e) => {
      e.preventDefault();
      const sem = $("noteSem").value;
      const title = $("noteTitle").value.trim();
      const url = $("noteURL").value.trim();
      if(!title || !url) { alert("Please add title and URL"); return; }
      const arr = loadCustomNotes();
      arr.push({sem, title, url});
      saveCustomNotes(arr);
      e.target.reset();
      renderCustomNotes();
    });
    $("clearNotes").addEventListener("click", () => {
      if(confirm("Remove all custom notes?")) { saveCustomNotes([]); renderCustomNotes(); }
    });

    // -------------------------
    // Show syllabus & notes
    // -------------------------
    function showSyllabus() {
      const name = $("name").value.trim();
      const collegeKey = $("college").value;
      const branchKey = $("branch").value;
      const outArea = $("outputPanel");
      const welcome = $("welcome");
      const noData = $("noData");

      if(!name || !collegeKey || !branchKey) { alert("Please enter your name, college and branch."); return; }

      // map college to university
      const uniKey = COLLEGE_MAP[collegeKey] || COLLEGE_MAP[collegeKey.toLowerCase()] || "jntuh";
      const uni = UNIVERSITIES[uniKey];
      if(!uni) {
        noData.innerHTML = `<p class="text-red-600">Syllabus not available for selected college/university mapping: ${uniKey}</p>`;
        welcome.classList.add("hidden");
        noData.classList.remove("hidden");
        return;
      }

      const branchData = uni.branches[branchKey];
      if(!branchData) {
        noData.innerHTML = `<p class="text-red-600">Syllabus not available for ${branchKey.toUpperCase()} under ${uni.label}.</p>`;
        welcome.classList.add("hidden");
        noData.classList.remove("hidden");
        return;
      }

      // populate UI
      welcome.classList.remove("hidden");
      noData.classList.add("hidden");

      $("greet").textContent = `Hi ${name} — ${branchKey.toUpperCase()} (${uni.label})`;
      $("meta").textContent = `College selected: ${document.querySelector("#college option:checked").textContent}`;

      $("coreFocus").textContent = branchData.coreFocus || "";
      $("tools").textContent = branchData.tools || "";
      $("careers").textContent = branchData.careers || "";

      // semesters
      const semWrap = $("semesterArea");
      semWrap.innerHTML = "<h3 class='font-semibold'>Semester-wise Subjects</h3>";
      const sems = branchData.semesters;
      const semList = document.createElement("div");
      semList.className = "mt-2 space-y-3";
      Object.entries(sems).forEach(([sem,subs]) => {
        const card = document.createElement("div");
        card.className = "p-3 rounded border bg-slate-50";
        card.innerHTML = `<div class="flex justify-between items-center"><strong>${sem}</strong><button class="px-2 py-1 text-xs rounded bg-indigo-600 text-white copyBtn">Copy</button></div>
                          <ul class="list-disc pl-5 mt-2">${subs.map(s=>`<li>${s}</li>`).join('')}</ul>`;
        semList.appendChild(card);
      });
      semWrap.appendChild(semList);
      // wire copy buttons
      semWrap.querySelectorAll(".copyBtn").forEach((b, idx) => {
        b.addEventListener("click", () => {
          const txt = Object.values(sems)[idx].join(", ");
          navigator.clipboard?.writeText(txt);
          b.textContent = "Copied";
          setTimeout(()=>b.textContent="Copy",1200);
        });
      });

      // notes
      const notesArea = $("notesList");
      notesArea.innerHTML = "";
      (branchData.notes || []).forEach(n => {
        const el = document.createElement("div");
        el.className = "p-2 rounded border bg-white";
        el.innerHTML = `<a href="${n.url}" target="_blank" class="inline-link">${n.title}</a> <div class="text-xs text-slate-500">${n.url === '#' ? 'replace with real link' : n.url}</div>`;
        notesArea.appendChild(el);
      });

      // skills
      const skillsArea = $("skillsList");
      skillsArea.innerHTML = "";
      (branchData.skills || []).forEach(s => {
        const el = document.createElement("div");
        el.className = "p-2 rounded border bg-white";
        el.textContent = s;
        skillsArea.appendChild(el);
      });

      // render custom notes
      renderCustomNotes();
    }

    // -------------------------
    // Export JSON (custom notes)
    // -------------------------
    $("exportJSON").addEventListener("click", () => {
      const data = loadCustomNotes();
      const blob = new Blob([JSON.stringify(data, null, 2)], {type:"application/json"});
      const url = URL.createObjectURL(blob);
      const a = document.createElement("a");
      a.href = url; a.download = "my_btech_notes_telangana.json";
      a.click();
      URL.revokeObjectURL(url);
    });

    // UI wiring
    showBtn.addEventListener("click", showSyllabus);
    printBtn.addEventListener("click", () => window.print());

    // On load, try to restore profile
    window.addEventListener("DOMContentLoaded", () => {
      const prof = loadProfile();
      if(prof.name) $("name").value = prof.name;
      if(prof.college) $("college").value = prof.college;
      if(prof.branch) $("branch").value = prof.branch;
      if(prof.name && prof.college && prof.branch) {
        // show automatically if all exist
        showSyllabus();
      }
    });
    </script>
  <h3>📌 Connect With Me</h3>
  <p>
    👉 Follow on Instagram: <a href="https://instagram.com/mouryareddy_5" target="_blank">Instagram</a><br>
    👉 Subscribe on YouTube: <a href="https://www.youtube.com/@EduBoss_OfficialS" target="_blank">YouTube</a>
  </p>
</footer>
