const projects = [
  {
    name: "نظام إدارة الطلاب",
    repo: "https://github.com/aslam/student-management",
    description: "واجهة منفصلة للطالب والأستاذ مع تخزين محلي."
  },
  {
    name: "مشروع تعليمي تجريبي",
    repo: "https://github.com/aslam/edu-demo",
    description: "نموذج بسيط لتجربة واجهات تعليمية."
  }
];

export default function ProjectsSection() {
  return (
    <div className="grid gap-4 md:grid-cols-2">
      {projects.map((project, index) => (
        <div key={index} className="border p-4 rounded-lg shadow-sm bg-white">
          <h3 className="text-lg font-semibold mb-2">{project.name}</h3>
          <p className="text-sm text-gray-600 mb-3">{project.description}</p>
          <a
            href={project.repo}
            target="_blank"
            rel="noopener noreferrer"
            className="inline-flex items-center text-blue-600 hover:underline"
          >
            <svg
              className="w-5 h-5 mr-1"
              fill="currentColor"
              viewBox="0 0 24 24"
            >
              <path d="M12 .5C5.73.5.5 5.73.5 12c0 5.08 3.29 9.39 7.86 10.93.58.11.79-.25.79-.56v-2.02c-3.2.7-3.87-1.54-3.87-1.54-.53-1.35-1.3-1.71-1.3-1.71-1.06-.72.08-.71.08-.71 1.17.08 1.78 1.2 1.78 1.2 1.04 1.78 2.73 1.27 3.4.97.11-.75.41-1.27.75-1.56-2.56-.29-5.26-1.28-5.26-5.7 0-1.26.45-2.3 1.2-3.11-.12-.29-.52-1.45.11-3.02 0 0 .98-.31 3.2 1.19a11.2 11.2 0 012.92-.39c.99.01 1.99.13 2.92.39 2.22-1.5 3.2-1.19 3.2-1.19.63 1.57.23 2.73.11 3.02.75.81 1.2 1.85 1.2 3.11 0 4.43-2.7 5.41-5.27 5.7.42.36.8 1.08.8 2.18v3.23c0 .31.21.67.8.56A10.5 10.5 0 0023.5 12C23.5 5.73 18.27.5 12 .5z" />
            </svg>
            GitHub Repository
          </a>
        </div>
      ))}
    </div>
  );
}
