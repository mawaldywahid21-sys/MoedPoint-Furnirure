# MoedPoint-Furnirure
MoedPoint is bast one of asian Store of Furniture that we use syari'ah Payment
import React from 'react';
import { Card, CardContent, CardHeader, CardTitle, CardDescription, CardFooter } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Button } from "@/components/ui/button";
import { Label } from "@/components/ui/label";
import { Sofa, Lock, Mail } from "lucide-react";

export default function LoginPage() {
  return (
    <div className="min-h-screen bg-slate-900 flex items-center justify-center p-4 relative overflow-hidden">
      {/* Elemen Dekoratif Latar Belakang (Efek Melayang) */}
      <div className="absolute top-1/4 -left-10 w-64 h-64 bg-purple-600/20 rounded-full blur-3xl animate-pulse"></div>
      <div className="absolute bottom-1/4 -right-10 w-80 h-80 bg-blue-600/20 rounded-full blur-3xl animate-pulse delay-700"></div>
      
      {/* Particle Decor */}
      <div className="absolute top-10 right-10 animate-bounce transition-all duration-1000">
        <Sofa className="text-white/10 w-20 h-20 rotate-12" />
      </div>
      <div className="absolute bottom-10 left-10 animate-bounce delay-300">
        <div className="w-4 h-4 bg-purple-500 rounded-full opacity-20"></div>
      </div>

      {/* Main Card dengan Efek Anti-Gravity */}
      <Card className="w-full max-w-md bg-white/95 backdrop-blur-sm shadow-[0_20px_50px_rgba(0,0,0,0.3)] border-none transform transition-all duration-700 hover:-translate-y-4 hover:shadow-[0_40px_80px_rgba(0,0,0,0.4)] animate-in fade-in zoom-in duration-1000">
        <CardHeader className="space-y-1 flex flex-col items-center pt-8">
          <div className="bg-purple-600 p-4 rounded-2xl mb-4 shadow-lg shadow-purple-500/50 animate-bounce [animation-duration:3s]">
            <Sofa className="h-10 w-10 text-white" />
          </div>
          <CardTitle className="text-3xl font-black text-slate-800 tracking-tight">
            Furniture <span className="text-purple-600">POS</span>
          </CardTitle>
          <CardDescription className="text-slate-500 font-medium">
            Sistem Kasir Melayang untuk Bisnis Anda
          </CardDescription>
        </CardHeader>
        
        <CardContent className="grid gap-5 px-8">
          <div className="grid gap-2 group">
            <Label htmlFor="email" className="text-slate-700 group-focus-within:text-purple-600 transition-colors">Email</Label>
            <div className="relative group">
              <Mail className="absolute left-3 top-3 h-4 w-4 text-slate-400 group-focus-within:text-purple-600 transition-colors" />
              <Input 
                id="email" 
                type="email" 
                placeholder="nama@perusahaan.com" 
                className="pl-10 border-slate-200 focus:border-purple-600 focus:ring-purple-600 transition-all bg-slate-50/50" 
              />
            </div>
          </div>
          
          <div className="grid gap-2 group">
            <div className="flex items-center justify-between">
              <Label htmlFor="password" className="text-slate-700 group-focus-within:text-purple-600 transition-colors">Kata Sandi</Label>
              <a href="#" className="text-xs text-purple-600 hover:underline font-semibold">Lupa sandi?</a>
            </div>
            <div className="relative group">
              <Lock className="absolute left-3 top-3 h-4 w-4 text-slate-400 group-focus-within:text-purple-600 transition-colors" />
              <Input 
                id="password" 
                type="password" 
                className="pl-10 border-slate-200 focus:border-purple-600 focus:ring-purple-600 transition-all bg-slate-50/50" 
              />
            </div>
          </div>
        </CardContent>
        
        <CardFooter className="flex flex-col gap-6 p-8">
          <Button className="w-full bg-purple-600 hover:bg-purple-700 text-white font-bold h-12 shadow-lg shadow-purple-500/30 transition-all hover:scale-[1.02] active:scale-95">
            Masuk Ke Sistem
          </Button>
          
          <div className="relative w-full">
            <div className="absolute inset-0 flex items-center"><span className="w-full border-t border-slate-100"></span></div>
            <div className="relative flex justify-center text-xs uppercase"><span className="bg-white px-2 text-slate-400">Atau</span></div>
          </div>

          <p className="text-sm text-center text-slate-500 font-medium">
            Belum punya akun? <a href="/register" className="text-purple-600 font-bold hover:text-purple-700 transition-colors">Daftar Toko</a>
          </p>
        </CardFooter>
      </Card>
      
      {/* Efek Pantulan di Bawah (Shadow Floor) */}
      <div className="absolute bottom-[-50px] left-1/2 -translate-x-1/2 w-[300px] h-[40px] bg-black/20 blur-[30px] rounded-[100%]"></div>
    </div>
  );
}