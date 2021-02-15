---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230655"
---
# New-AzDataFactoryEncryptValue

## SYNOPSIS
Krypterar känsliga data.

## SYNTAX

### ByFactoryName (standard)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzDataFactoryEncryptValue** krypterar känsliga data, till exempel ett lösenord eller en Microsoft SQL Server-anslutningssträng, och returnerar ett krypterat värde.

## EXEMPEL

### Exempel 1: Kryptera en icke-ODBC-anslutningssträng
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Det första kommandot använder cmdleten ConvertTo-SecureString för att konvertera den angivna anslutningssträngen till ett **SecureString-objekt** och lagrar sedan objektet i $Value variabeln.
Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .
Tillåtna värden: SQL Server- eller Oracle-anslutningssträng.
Det andra kommandot skapar ett krypterat värde för objektet som lagras i $Value för den angivna data factory, gateway, resursgrupp och länkade tjänsttypen.

### Exempel 2: Kryptera en icke-ODBC-anslutningssträng som använder Windows-autentisering.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

Det första kommandot använder **ConvertTo-SecureString** för att konvertera den angivna anslutningssträngen till ett säkert strängobjekt och lagrar sedan objektet i den $Value variabeln.
Det andra kommandot använder cmdleten Get-Credential samla in Windows-autentiseringen (användarnamn och lösenord) och lagrar sedan **PSCredential-objektet** i $Credential variabeln.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .
Det tredje kommandot skapar ett krypterat värde för objektet som lagras i $Value och $Credential för den angivna datakällan, gatewayen, resursgruppen och den länkade tjänsttypen.

### Exempel 3: Kryptera servernamn och autentiseringsuppgifter för länkade filsystemtjänster
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Det första kommandot använder **ConvertTo-SecureString** för att konvertera den angivna strängen till en säker sträng och lagrar sedan objektet i $Value variabeln.
Det andra kommandot använder **Get-Credential** för att samla in Windows-autentisering (användarnamn och lösenord) och lagrar sedan **PSCredential-objektet** i $Credential variabeln.
Det tredje kommandot skapar ett krypterat värde för objektet som lagras i $Value och $Credential för den angivna datakällan, gatewayen, resursgruppen och den länkade tjänsttypen.

### Exempel 4: Kryptera autentiseringsuppgifter för HDFS-länkade tjänster
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Kommandot **ConvertTo-SecureString** konverterar den angivna strängen till en säker sträng.
Med **kommandot Nytt objekt** skapas ett PSCredential-objekt med hjälp av säkra användarnamns- och lösenordssträngar.
I stället kan du använda kommandot Hämta autentiseringsuppgifter för att samla in **Windows-autentisering** (användarnamn och lösenord) och sedan lagra det returnerade **PSCredential-objektet** i $credential-variabeln som visat i tidigare exempel.
Kommandot **New-AzDataFactoryEncryptValue** skapar ett krypterat värde för objektet som lagras i $Credential för angiven data factory, gateway, resursgrupp och länkad tjänsttyp.

### Exempel 5: Kryptera autentiseringsuppgifter för ODBC-länkade tjänster
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Kommandot **ConvertTo-SecureString** konverterar den angivna strängen till en säker sträng.
Kommandot **New-AzDataFactoryEncryptValue** skapar ett krypterat värde för objektet som lagras i $Value för angiven data factory, gateway, resursgrupp och länkad tjänsttyp.

## PARAMETERS

### -AuthenticationType
Anger vilken typ av autentisering som ska användas för att ansluta till datakällan.
De godtagbara värdena för den här parametern är:
- Windows
- Grundläggande
- Anonym.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Anger vilka autentiseringsuppgifter för Windows -autentisering (användarnamn och lösenord) som ska användas.
Den här cmdleten krypterar de autentiseringsuppgifter du anger här.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Anger databasnamnet för den länkade tjänsten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
Anger ett **PSDataFactory-objekt.**
Den här cmdleten krypterar data för den data factory som den här parametern anger.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Anger namnet på en data factory.
Den här cmdleten krypterar data för den data factory som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayName
Anger gatewayens namn.
Den här cmdleten krypterar data för gatewayen som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
Anger den del av ODBC-anslutningssträngen (Open Database Connectivity) som inte är en autentiseringsdel.
Den här parametern gäller endast för den ODBC-länkade tjänsten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-resursgrupp.
Den här cmdleten krypterar data för gruppen som parametern anger.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server
Anger servernamnet för den länkade tjänsten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Anger den länkade tjänsttypen.
Den här cmdleten krypterar data för den länkade tjänsttyp som den här parametern anger.
De godtagbara värdena för den här parametern är:
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOraserviceLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Värde
Anger värdet som ska krypteras.
Använd en anslutningssträng för en lokal SQL Server-länkad tjänst och en lokal Oracle-länkad tjänst.
För en lokal ODBC-länkad tjänst använder du autentiseringsdelen av anslutningssträngen.
Om filsystemet är lokalt på gatewaydatorn använder du Local eller localhost för en lokal filsystemslänktjänst, och om filsystemet finns på en annan server än gatewaydatorn använder du \\ \\ servernamn.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## UTDATA

### System.String

## ANTECKNINGAR
* Nyckelord: azure, azurerm, arm, resource, management, manager, data, factories

## RELATERADE LÄNKAR

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


