# pene

import 'package:flutter/material.dart';

void main() => runApp(MisIconos());

class MisIconos extends StatelessWidget {
  const MisIconos({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("Luis Herrera"),
          titleTextStyle: TextStyle(color: Color(0xff1335cf), fontSize: 20),
          centerTitle: true,
          backgroundColor: Color(0xff2c2a2a),
        ),
        body: Center(
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
              Text("LUIS HERRERA 22308051281207",
                  style: TextStyle(
                      fontSize: 20,
                      fontStyle: FontStyle.italic,
                      color: Color(0xd10949d2))),
              // Primera fila
              Row(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: <Widget>[
                  IconWithSubtitle(icon: Icons.home, subtitle: 'Inicio'),
                  IconWithSubtitle(icon: Icons.favorite, subtitle: 'Favoritos'),
                  IconWithSubtitle(icon: Icons.star, subtitle: 'Destacado'),
                ],
              ),
              SizedBox(height: 20), // Espacio entre las filas
              // Segunda fila
              Row(
                mainAxisAlignment: MainAxisAlignment.center,
                children: <Widget>[
                  IconWithSubtitle(icon: Icons.tiktok, subtitle: 'TikTok'),
                  IconWithSubtitle(icon: Icons.snapchat, subtitle: 'Snapchat'),
                  IconWithSubtitle(icon: Icons.sailing, subtitle: 'Barco'),
                ],
              ),
            ],
          ),
        ),
      ),
    );
  }
}

// Widget personalizado para un ícono con subtítulo
class IconWithSubtitle extends StatelessWidget {
  final IconData icon;
  final String subtitle;

  IconWithSubtitle({required this.icon, required this.subtitle});

  @override
  Widget build(BuildContext context) {
    return Column(
      children: <Widget>[
        Icon(icon, size: 50.0, color: Colors.blue),
        SizedBox(height: 8), // Espacio entre el ícono y el subtítulo
        Text(subtitle, style: TextStyle(fontSize: 16)),
      ],
    );
  }
}
