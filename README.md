import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input";

export default function SportsViewerSite() { return ( <div className="min-h-screen bg-gray-100 text-gray-900"> <header className="bg-white shadow p-6 flex justify-between items-center"> <h1 className="text-2xl font-bold">Fire Guyz VB</h1> <nav className="space-x-4"> <a href="#home" className="hover:underline">Home</a> <a href="#members" className="hover:underline">Members</a> <a href="#games" className="hover:underline">Games</a> </nav> </header>

<main className="p-6 space-y-10">
    <section id="home" className="text-center space-y-4">
      <h2 className="text-3xl font-semibold">Welcome to Fire Guyz VB</h2>
      <p className="text-lg">Follow your favorite sports team and catch all the latest updates!</p>
      <img
        src="/team-photo.jpg"
        alt="Team Photo"
        className="mx-auto rounded-2xl shadow-lg max-w-xl"
      />
    </section>

    <section id="members">
      <h3 className="text-2xl font-semibold mb-4">Team Members</h3>
      <div className="grid grid-cols-2 md:grid-cols-4 gap-4">
        {["Ali", "John", "Moeed", "Usman"].map((member, i) => (
          <Card key={i} className="text-center p-4">
            <CardContent>
              <h4 className="font-bold text-lg">{member}</h4>
            </CardContent>
          </Card>
        ))}
      </div>
    </section>

    <section id="games">
      <h3 className="text-2xl font-semibold mb-4">Upcoming Games</h3>
      <div className="space-y-4">
        <Card>
          <CardContent>
            <p className="font-semibold">Fire Guyz VB vs Thunder Smashers</p>
            <p>Date: May 25, 2025</p>
          </CardContent>
        </Card>
        <Card>
          <CardContent>
            <p className="font-semibold">Fire Guyz VB vs Heat Blazers</p>
            <p>Date: June 2, 2025</p>
          </CardContent>
        </Card>
      </div>
    </section>
  </main>
</div>

); }

