import { motion } from "framer-motion";

export default function Portfolio() {
  return (
    <div className="relative min-h-screen bg-gray-50 overflow-hidden font-sans flex flex-col items-center justify-center text-center p-6">
      {/* Animated gradient blobs */}
      <motion.div
        className="absolute top-10 left-10 w-72 h-72 bg-gradient-to-tr from-pink-400 via-yellow-300 to-purple-400 rounded-full filter blur-3xl opacity-70"
        animate={{ x: [0, 50, 0], y: [0, -30, 0] }}
        transition={{ repeat: Infinity, duration: 8 }}
      />
      <motion.div
        className="absolute bottom-20 right-10 w-96 h-96 bg-gradient-to-tr from-green-300 via-blue-300 to-purple-300 rounded-full filter blur-3xl opacity-70"
        animate={{ x: [0, -60, 0], y: [0, 40, 0] }}
        transition={{ repeat: Infinity, duration: 10 }}
      />
      <motion.div
        className="absolute top-1/3 left-1/4 w-64 h-64 bg-gradient-to-tr from-orange-400 via-pink-300 to-red-400 rounded-full filter blur-3xl opacity-70"
        animate={{ x: [0, 40, 0], y: [0, -50, 0] }}
        transition={{ repeat: Infinity, duration: 9 }}
      />

      {/* Main content */}
      <header className="relative z-10">
        <h1 className="text-4xl md:text-6xl font-extrabold text-gray-800">
          HEY I AM <span className="text-blue-600">HERY SILVERIO</span>
        </h1>
        <p className="mt-2 text-xl text-gray-600">Software Developer</p>
      </header>

      <main className="relative z-10 max-w-3xl mt-6">
        {/* Projects */}
        <section className="mb-8">
          <h2 className="text-2xl font-semibold mb-3">Projects</h2>
          <ul className="list-disc list-inside text-left inline-block space-y-2">
            <li><strong>Bettertube</strong> – A YouTube experience with enhanced features.</li>
            <li><strong>Betterbloxorz</strong> – A modern remake of the classic puzzle game.</li>
            <li><strong>Content Filter App</strong> – A tool to filter and manage online content.</li>
          </ul>
        </section>

        {/* Skills */}
        <section>
          <h2 className="text-2xl font-semibold mb-3">Skills</h2>
          <div className="flex flex-wrap gap-3 justify-center">
            {["JavaScript","Python","Java","Kotlin","C#","TypeScript","Swift","GitHub","SQL & NoSQL","Node.js","Bootstrap"].map(skill => (
              <span key={skill} className="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm font-medium shadow">
                {skill}
              </span>
            ))}
          </div>
        </section>
      </main>

      <footer className="relative z-10 mt-8 text-gray-600">
        © {new Date().getFullYear()} Hery Silverio. All rights reserved.
      </footer>
    </div>
  );
}
