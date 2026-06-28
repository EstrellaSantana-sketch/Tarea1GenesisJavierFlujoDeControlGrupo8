# Tarea1GenesisJavierFlujoDeControlGrupo8
Tarea 1 primera Unidad sobre el Flujo De Control
using System;
class Program
{
    static void Main()
    {
        Console.WriteLine("calcular el prestamo");
        Console.WriteLine("--------------");

        Console.WriteLine("ingrese la cantidad que desea tomar prestado");
        double monto = Convert.ToDouble(Console.ReadLine());

        Console.WriteLine("ingresa tu tasa de interes anual (en%)");
        double tazaAnual = Convert.ToDouble(Console.ReadLine());

        Console.WriteLine("cuanto tiempo desea durar pagando");
        double meses = Convert.ToDouble(Console.ReadLine());

        double tasamensual = (tazaAnual / 100) / 12;
        double cuotabase = monto * (tasamensual * Math.Pow(1 + tasamensual, meses)) / (Math.Pow(1 + tasamensual, meses) - 1);


        double tasaSegurovida = 0.0015;
        double costoSeguromensual = monto * tasaSegurovida;
        double cuotaTotal = cuotabase + costoSeguromensual;


        Console.WriteLine(" --- RESUMEN DEL PRÉSTAMO ---");
        Console.WriteLine($"• Monto solicitado:      RD${monto:F2}");
        Console.WriteLine($"• Cuota Base (Capital+Interés): RD${cuotabase:F2}");
        Console.WriteLine($"• Seguro de Vida (Aprox):RD${costoSeguromensual:F2}");
        Console.WriteLine("-----------------------------------------");
        Console.WriteLine($" CUOTA TOTAL MENSUAL:  RD${cuotaTotal:F2}");

        Console.WriteLine("Presiona cualquier tecla para salir...");
        Console.ReadKey();
    }
}

