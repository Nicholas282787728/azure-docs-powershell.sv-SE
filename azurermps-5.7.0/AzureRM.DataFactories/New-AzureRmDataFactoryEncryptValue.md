---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: ffdd124658ecaadfdd1772fb03a3e8c40254f698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578215"
---
# New-AzureRmDataFactoryEncryptValue

## Sammanfattning
Krypterar känsliga data.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByFactoryName (standard)
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Den **nya** cmdleten AzureRmDataFactoryEncryptValue krypterar känsliga data, till exempel ett lösen ord eller en Microsoft SQL Server-anslutningssträng, och returnerar ett krypterat värde.

## BESKRIVS

### Exempel 1: kryptera en icke-ODBC-anslutningssträng
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

I det första kommandot används ConvertTo-SecureString cmdlet för att konvertera den angivna anslutnings strängen till ett **SecureString** -objekt och sedan lagras objektet i $Value-variabeln.
Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .
Tillåtna värden: SQL Server eller Oracle-anslutningssträng.

Det andra kommandot skapar ett krypterat värde för det objekt som lagras i $Value för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.

### Exempel 2: kryptera en icke-ODBC-anslutningssträng som använder Windows-inloggning.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

Det första kommandot använder **ConvertTo-SecureString** för att konvertera den angivna anslutnings strängen till ett säkert String-objekt och lagrar sedan objektet i variabeln $Value.

Det andra kommandot använder cmdleten Get-Credential för att samla in Windows-inloggningen (användar namn och lösen ord) och lagrar sedan **PSCredential** -objektet i $Credential-variabeln.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .

Det tredje kommandot skapar ett krypterat värde för det objekt som lagras i $Value och $Credential för angiven data fabrik, Gateway, resurs grupp och länkad tjänst typ.

### Exempel 3: kryptera Server namn och autentiseringsuppgifter för den länkade tjänsten för fil system
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Det första kommandot använder **ConvertTo-SecureString** för att konvertera den angivna strängen till en säker sträng och lagrar sedan objektet i variabeln $Value.

Det andra kommandot används för att samla in Windows-autentisering (användar namn och lösen ord) och lagrar sedan **PSCredential** **-** objektet i variabeln $Credential.

Det tredje kommandot skapar ett krypterat värde för det objekt som lagras i $Value och $Credential för angiven data fabrik, Gateway, resurs grupp och länkad tjänst typ.

### Exempel 4: krypterar autentiseringsuppgifter för den länkade tjänsten HDFS
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Med kommandot **ConvertTo-SecureString** konverteras den angivna strängen till en säker sträng.
Kommandot **ny-objekt** skapar ett PSCredential-objekt med hjälp av de säkra användar-och lösen ords strängarna.
I stället kan du använda kommandot **Hämta-autentiseringsuppgifter** för att samla in Windows-autentisering (användar namn och lösen ord) och sedan lagra det returnerade **PSCredential** -objektet i $Credential variabel enligt föregående exempel.

Med kommandot **ny-AzureRmDataFactoryEncryptValue** skapas ett krypterat värde för det objekt som lagras i $Credential för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.

### Exempel 5: krypterings-autentiseringsuppgifter för ODBC-länkad tjänst
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Med kommandot **ConvertTo-SecureString** konverteras den angivna strängen till en säker sträng.

Med kommandot **ny-AzureRmDataFactoryEncryptValue** skapas ett krypterat värde för det objekt som lagras i $Value för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.

## MALLPARAMETRAR

### -AuthenticationType
Anger vilken typ av verifikation som ska användas för att ansluta till data källan.
De acceptabla värdena för den här parametern är:

- Windows
- Basisk
- Anonym.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Autentiseringsuppgift
Anger Windows autentiseringsinformation (användar namn och lösen ord) som ska användas.
Denna cmdlet krypterar de autentiseringsuppgifter du anger här.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Databas
Anger databas namnet på den länkade tjänsten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
Anger ett **PSDataFactory** -objekt.
Denna cmdlet krypterar data för data fabriken som den här parametern anger.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Anger namnet på en data fabrik.
Denna cmdlet krypterar data för data fabriken som den här parametern anger.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayName
Anger namnet på gatewayen.
Denna cmdlet krypterar data för den gateway som den här parametern anger.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
Anger icke-Credential-delen av ODBC-anslutningssträng (Open Database Connectivity).
Den här parametern används endast för den länkade ODBC-tjänsten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-adressresurs.
Denna cmdlet krypterar data för gruppen som den här parametern anger.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server
Anger Server namnet på den länkade tjänsten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Skriv
Anger den länkade tjänst typen.
Denna cmdlet krypterar data för den länkade tjänst typen som den här parametern anger.
De acceptabla värdena för den här parametern är:

- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: String
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
Anger det värde som ska krypteras.
Använd en anslutnings sträng för en lokal SQL Server-länkad tjänst och en lokal Oracle-länkad tjänst.
För en lokal ODBC-länkad tjänst kan du använda Credential-delen av anslutnings strängen.
För den länkade tjänsten för lokala fil system, om fil systemet är lokalt för gateway-datorn, Använd lokal eller localhost, och om fil systemet finns på en annan server än gateway-datorn, Använd \\ \\ Server namn.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### System. String

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer

## RELATERADE LÄNKAR

[New-AzureRmDataFactoryEncryptValue](./New-AzureRmDataFactoryEncryptValue.md)


