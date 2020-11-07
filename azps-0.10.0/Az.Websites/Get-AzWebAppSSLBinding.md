---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923353"
---
# Get-AzWebAppSSLBinding

## Sammanfattning
Hämtar ett Azure Web App-certifikat för SSL-bindning.

## FRÅGESYNTAXEN

### S
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzWebAppSSLBinding** får en SSL-bindning (Secure Sockets Layer) för en Azure Web App.
SSL-bindningar används för att koppla ett webb program till ett uppladdat certifikat.
Webb program kan bindas till flera certifikat.

## BESKRIVS

### Exempel 1: Hämta SSL-bindningar för ett webb program
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Det här kommandot hämtar SSL-bindningarna för Web App-ContosoWebApp, som är kopplat till resurs gruppen ContosoResourceGroup.

### Exempel 2: använda en objekt referens för att få SSL-bindningar för ett webb program
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

Kommandona i det här exemplet hämtar också SSL-bindningarna för Web App-ContosoWebApp; i det här fallet används en objekt referens i stället för namnet på den associerade resurs gruppen.
Den här objekt referensen skapas av det första kommandot i exemplet, som använder funktionen **Get-AzWebApp** för att skapa en objekt referens till webb programmet som heter ContosoWebApp.
Objekt referensen lagras i en variabel som heter $WebApp.

Den här variabeln och cmdleten **Get-AzWebAppSSLBinding** används sedan av det andra kommandot för att hämta SSL-bindningarna.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på SSL-bindningen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen som certifikatet har tilldelats till.

Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger en distributions plats för webbprogram.
Använd Get-AzWebAppSlot cmdlet för att få en distributions plats.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Anger ett webb program.
Om du vill hämta en webbapp använder du Get-AzWebApp cmdlet.

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Anger namnet på den webbapp som den här cmdleten får SSL-bindningar från.

Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Webbplatsmallar
Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


