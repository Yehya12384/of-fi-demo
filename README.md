# of-fi-demo
Offline content viewer for social platforms
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Of-Fi',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: const MyHomePage(),
      debugShowCheckedModeBanner: false,
    );
  }
}

class MyHomePage extends StatelessWidget {
  const MyHomePage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Of-Fi'),
      ),
      body: GridView.count(
        crossAxisCount: 2,
        padding: const EdgeInsets.all(16),
        crossAxisSpacing: 16,
        mainAxisSpacing: 16,
        children: const [
          AppIcon(title: 'TikTok', icon: Icons.music_note),
          AppIcon(title: 'Instagram', icon: Icons.camera_alt),
          AppIcon(title: 'YouTube', icon: Icons.ondemand_video),
          AppIcon(title: 'Telegram', icon: Icons.send),
          AppIcon(title: 'WhatsApp', icon: Icons.chat),
        ],
      ),
    );
  }
}

class AppIcon extends StatelessWidget {
  final String title;
  final IconData icon;

  const AppIcon({super.key, required this.title, required this.icon});

  @override
  Widget build(BuildContext context) {
    return Column(
      mainAxisAlignment: MainAxisAlignment.center,
      children: [
        Icon(icon, size: 50, color: Colors.blue),
        const SizedBox(height: 8),
        Text(title, style: const TextStyle(fontSize: 16)),
      ],
    );
  }
}
name: of_fi
description: A new Flutter project.

publish_to: 'none'

version: 1.0.0+1

environment:
  sdk: ">=3.3.3 <4.0.0"

dependencies:
  flutter:
    sdk: flutter
  cupertino_icons: ^1.0.2

dev_dependencies:
  flutter_test:
    sdk: flutter

  flutter_lints: ^3.0.0

flutter:
  uses-material-design: true
