# Praktikum 14

Töötamsime Azure VM-iga
Alustasin väga hästi, kõik oli tore.

<img width="491" alt="OS23_lab1a" src="https://github.com/Voronkov2004/UT-Operatsioon/blob/main/Praks%2014-1.png?raw=true">

<img width="491" alt="OS23_lab1a" src="https://github.com/Voronkov2004/UT-Operatsioon/blob/main/Praks%2014-2.png?raw=true">

<img width="491" alt="OS23_lab1a" src="https://github.com/Voronkov2004/UT-Operatsioon/blob/main/Praks%2014-3.png?raw=true">

<img width="491" alt="OS23_lab1a" src="https://github.com/Voronkov2004/UT-Operatsioon/blob/main/Praks%2014-4%20.png?raw=true">

Ma proovisin seda parandada 2 tundi. Siin on käsud mida ma proovisin:
New-SelfSignedCertificate -DnsName "localhost" -CertStoreLocation "Cert:\LocalMachine\My"

Remove-Item -Path WSMan:\localhost\Listener\Listener_1234567890 -Force (Siin ma vahetasin Listener õigele numbrile)

New-Item -Path WSMan:\localhost\Listener -Transport HTTPS -Address * -Force

Remove-NetFirewallRule -Name "Allow WinRM HTTPS"

Get-ChildItem -Path Cert:\LocalMachine\My

$cert = New-SelfSignedCertificate -DnsName "<your_dns_name>" -CertStoreLocation "Cert:\LocalMachine\My"

$thumbprint = $cert.Thumbprint
New-Item -Path WSMan:\localhost\Listener -Transport HTTPS -Address * -CertificateThumbprint $thumbprint -Force

Get-NetConnectionProfile

Set-NetConnectionProfile -InterfaceIndex <InterfaceIndex> -NetworkCategory Private

Ja seal on väga palju veel, aga mitte midagi ei saanud sellega teha.
