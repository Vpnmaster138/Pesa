import React, { useState } from "react";
import {
  Tabs,
  TabsList,
  TabsTrigger,
  TabsContent,
} from "@/components/ui/tabs";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Button } from "@/components/ui/button";

export default function App() {
  const [isLoggedIn, setIsLoggedIn] = useState(false);
  const [username, setUsername] = useState("");
  const [password, setPassword] = useState("");

  const handleLogin = () => {
    if (username === "admin" && password === "admin") {
      setIsLoggedIn(true);
    } else {
      alert("Invalid credentials");
    }
  };

  if (!isLoggedIn) {
    return (
      <div className="p-4">
        <h2 className="text-xl font-bold mb-4">Login</h2>
        <Input
          type="text"
          placeholder="Username"
          value={username}
          onChange={(e) => setUsername(e.target.value)}
          className="mb-2"
        />
        <Input
          type="password"
          placeholder="Password"
          value={password}
          onChange={(e) => setPassword(e.target.value)}
          className="mb-4"
        />
        <Button onClick={handleLogin}>Login</Button>
      </div>
    );
  }

  return (
    <div className="p-4">
      <h2 className="text-2xl font-bold mb-4">
        Karibu kwenye Dashboard yako
        {" "}💰💵💶💷🪙
      </h2>
      <Tabs defaultValue="overview">
        <TabsList>
          <TabsTrigger value="overview">Overview</TabsTrigger>
          <TabsTrigger value="bonuses">Bonuses</TabsTrigger>
          <TabsTrigger value="withdraw">Withdraw</TabsTrigger>
        </TabsList>

        <TabsContent value="overview">
          <Card>
            <CardContent className="p-4">
              Hapa ni muhtasari wa akaunti yako.
            </CardContent>
          </Card>
        </TabsContent>

        <TabsContent value="bonuses">
          <Card>
            <CardContent className="p-4">
              Bonasi zako zitaonekana hapa.
            </CardContent>
          </Card>
        </TabsContent>

        <TabsContent value="withdraw">
          <Card>
            <CardContent className="p-4">
              Unaweza kutoa pesa hapa.
            </CardContent>
          </Card>
        </TabsContent>
      </Tabs>
    </div>
  );
}
