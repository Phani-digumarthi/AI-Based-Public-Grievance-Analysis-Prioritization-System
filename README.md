📢 AI-Based Public Grievance Analysis & Prioritization SystemA robust MERN Stack web application designed to streamline civic grievance redressal. This platform allows citizens to lodge complaints with multimedia evidence (Images & Audio) and provides authorities with a dashboard to visualize and manage issues.🚀 Key Features🏛️ Citizen PortalMultimedia Support: Upload photos and record voice notes as evidence.Smart Forms: Manual entry for grievance description, category, and priority.History Tracking: View the status of past complaints.👮 Admin DashboardInteractive Heatmap: Visualize grievance hotspots using Leaflet Maps.Status Management: Filter by Priority (Immediate, High, Medium, Low) and Status (Pending, Resolved).Evidence Review: Direct access to uploaded images and audio files.🛠️ Tech StackFrontend: Next.js (React), Tailwind CSS, Lucide Icons, React-LeafletBackend: Node.js, Express.jsDatabase: MongoDB (Mongoose)File Storage: Multer (Local storage in server/uploads)⚙️ PrerequisitesBefore running the project, ensure you have the following installed:Node.js (v18+)MongoDB (Local or Atlas URL)Git📥 Installation Guide1. Clone the RepositoryBashgit clone https://github.com/Phani-digumarthi/AI-Based-Public-Grievance-Analysis-Prioritization-System.git
cd AI-Based-Public-Grievance-Analysis-Prioritization-System
2. Backend Setup (Server)The backend runs on Port 5000.Navigate to the server folder:Bashcd server
Install dependencies:Bashnpm install
Configure Environment:Create a .env file inside the server/ folder and add:Code snippetPORT=5000
MONGO_URI=mongodb://localhost:27017/civic_connect_db
(Note: Replace MONGO_URI with your MongoDB Atlas string if using cloud database)Start the Server:Bashnode index.js
✅ Console Output: Server running on port 5000 & MongoDB Connected3. Frontend Setup (Web Portal)The frontend runs on Port 3000.Open a new terminal and navigate to the web portal:Bashcd web-portal
Install dependencies:Bashnpm install
Start the Development Server:Bashnpm run dev
✅ Access App: Open http://localhost:3000 in your browser.📂 Project Structure├── server/                 # Backend (Node.js + Express)
│   ├── models/             # Mongoose Database Schemas
│   ├── uploads/            # Storage for uploaded Images/Audio
│   ├── index.js            # Main Server File
│   └── .env                # Environment Variables
│
└── web-portal/             # Frontend (Next.js)
    ├── app/
    │   ├── admin/          # Admin Dashboard & Login
    │   └── citizen/        # Citizen Lodge & History Pages
    ├── components/         # Reusable UI (Maps, Forms)
    └── public/             # Static Assets
🛡️ API EndpointsMethodEndpointDescriptionPOST/api/grievances/submitSubmit a new grievance with filesGET/api/grievancesFetch all grievances for Admin/HistoryPUT/api/grievances/:idUpdate grievance status (Resolve)📝 UsageCitizen: Log in, select "Lodge Grievance", fill the form, upload an image/audio, and click Submit.Admin: Log in to the Dashboard to view the live map and list of pending issues. Click "View Details" to see the uploaded evidence.
