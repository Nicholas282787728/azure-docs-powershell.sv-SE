---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093241"
---
# New-AzureStorSimpleNetworkConfig

## Sammanfattning
Förbereder ett nätverks konfigurations objekt.

## FRÅGESYNTAXEN

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorSimpleNetworkConfig** förbereder ett nätverks konfigurations objekt för överföring till cmdleten **set-AzureStorSimpleDevice** .
Ange parametern *Controller0IPAddress* och *Controller1IPAddress* för Data0-gränssnittet.
Data0 stöder bara tre inställningar: *Controller0IPAddress* , *Controller1IPAdress* och *EnableIscsi*.

## BESKRIVS

### Exempel 1: Konfigurera ett Data0 gränssnitt
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

Det här kommandot skapar nätverks konfiguration för Data0-gränssnittet.
Det här kommandot anger parametrarna *Controller0IPv4Address* , *Controller1IPv4Address* och *EnableIscsi* .
Denna cmdlet kan konfigurera Data0 för endast dessa tre parametrar.

### Exempel 2: Konfigurera ett annat gränssnitt än Data0 ett
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

Det här kommandot konfigurerar värdet data1.

### Exempel 3: ändra en konfiguration för en enhet
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

Det första kommandot skapar en nätverks konfiguration för Data0-gränssnittet.
Det här kommandot anger parametrarna *Controller0IPv4Address* , *Controller1IPv4Address* och *EnableIscsi* .
Kommandot sparar resultatet i variabeln $NetworkConfigData 0.

I det andra kommandot används cmdleten **Get-AzureStorSimpleDevice** och en cmdlet för **WHERE-objekt** för att hämta en online StorSimple-enhet och sedan lagras den i $OnlineDevice variabel.

Det sista kommandot ändrar konfigurationen för enheten som har angivet enhets-ID genom att använda cmdleten **set-AzureStorSimpleDevice** .
Kommandot använder det konfigurations objekt som den aktuella cmdleten skapade i det första kommandot.

## MALLPARAMETRAR

### -Controller0IPv4Address
Anger IPv4-adressen för Controller 0.
Ange endast den här parametern för Data0-gränssnittet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Controller1IPv4Address
Anger IPv4-adressen för styrenhet 1.
Ange endast den här parametern för Data0-gränssnittet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCloud
Anger om molnet ska aktivera gränssnittet.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableIscsi
Anger om du vill aktivera Internet SCSI (ISCSI) för gränssnittet.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InterfaceAlias
Anger gränssnitts Ali Aset för gränssnitt som denna cmdlet tillhandahåller inställningar för.
Giltiga värden är från Data0 till Data5.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Address
Anger IPv4-adressen för gränssnittet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Gateway
Anger IPv4-adressen för en gateway.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Netmask
Anger gränssnittets IPv4-nätmask.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv6Gateway
Anger IPv6-Gateway för gränssnittet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv6Prefix
Anger IPv6-prefixet för gränssnittet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger en Azure-profil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### NetworkConfig
Denna cmdlet returnerar ett NetworkConfig-objekt som innehåller följande egenskaper: 

- **IsIscsiEnabled** ( **boolesk** ) 
- **IsCloudEnabled** ( **boolesk** )
- **Controller0IPv4Address** ( **IPAddress** ) 
- **Controller1IPv4Address** ( **IPAddress** ) 
- **IPv6Gateway** ( **IPAddress** ) 
- **IPv4Gateway** ( **IPAddress** ) 
- **IPv4Address** ( **IPAddress** ) 
- **IPv6Prefix** ( **sträng** )
- **IPv4Netmask** ( **IPAddress** ) 
- **InterfaceAlias** ( **NetInterfaceId** )

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureStorSimpleDevice](./Set-AzureStorSimpleDevice.md)

[Get-AzureStorSimpleDevice](./Get-AzureStorSimpleDevice.md)


