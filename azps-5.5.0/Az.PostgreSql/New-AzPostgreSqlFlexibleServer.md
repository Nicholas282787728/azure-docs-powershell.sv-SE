---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c658780407454f780ccbd00cb824dd1032f3463d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227222"
---
# New-AzPostgreSqlFlexibleServer

## SYNOPSIS
Skapar en ny server.

## SYNTAX

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## BESKRIVNING
Skapar en ny server.

## EXEMPEL

### Exempel 1: Skapa en ny PostgreSql flexibel server med argument
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### Exempel 2: Skapa en ny PostgreSql-flexibel server med standardinställning
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

Den här cmdleten skapar PostgreSql-flexibel server med standardparametervärden och etablerar servern i ett nytt virtuellt nätverk och har ett undernät delegerat till servern.
Standardvärdena för platsen är Väst-US 2, SKU är Standard_D2s_v3, SKU-nivån är GeneralPurpose och lagringsstorleken är 128GiB.


Om du vill hitta det automatiskt genererade lösenordet för servern använder du ConvertFrom-SecureString konvertera egenskapen SecuredPassword till oformaterad text.
(Till exempel $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)

### Exempel 3: Skapa en ny PostgreSql-flexibel server med virtuellt nätverk
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

Med den här cmdleten skapas PostgreSql-flexibel server med vnet-ID eller vnet-namn som tillhandahålls av en användare.
Om det virtuella nätverket inte finns skapar cmdleten en.

### Exempel 4: Skapa en ny PostgreSql-flexibel server med namn på virtuellt nätverk och undernät
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

Med den här cmdleten skapas PostgreSql-flexibel server med vnet-namn, undernätsnamn, vnet-prefix och undernätsprefix.
Om det virtuella nätverket och undernätet inte finns skapar cmdleten ett.

### Exempel 7: Skapa en ny PostgreSql-flexibel server med offentlig åtkomst till alla IP-adresser
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

Med den här cmdleten skapas PostgreSql-flexibel server som är öppen för alla IP-adresser.

### Exempel 8: Skapa en ny PostgreSql flexibel server med brandvägg
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

Den här cmdleten skapar PostgreSql-flexibel server som är öppen för angivna IP-adresser.

## PARAMETERS

### -AdministratorLoginPassword
Administratörens lösenord.
Minst 8 tecken och högst 128 tecken.
Lösenordet måste innehålla tecken från tre av följande kategorier: versaler på engelska, gemener på engelska, siffror och icke-alfanumeriska tecken.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministratorUserName
Administratörsnamn för servern.
När den har angetts kan den inte ändras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -As Ent fån
Kör kommandot som ett jobb.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupRetentionDay
Bevarandedagar för säkerhetskopiering för servern.
Antalet dagar är mellan 7 och 35.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Platsen som resursen finns i.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Namnet på servern.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Kör kommandot asynkront.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicAccess
Avgör den offentliga åtkomsten.
Ange en ip-adress eller ett intervall med IP-adresser som ska ingå i listan över tillåtna IP-adresser.
IP-adressintervallen måste vara streckavgränsade och får inte innehålla blanksteg.
Om du anger 0.0.0.0 tillåts offentlig åtkomst från alla resurser som är distribuerade i Azure för att få åtkomst till servern.
Om du inte anger någon IP-adress anges servern i offentligt åtkomstläge, men det skapas ingen brandväggsregel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen som innehåller resursen. Du kan hämta det här värdet från Azure Resource Manager API eller portalen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Namnet på SKU:n, vanligtvis nivå + familj + kärnor, t.ex. Standard_B1ms, Standard_D2ds_v4.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuTier
Beräkna servernivån.
Godkända värden: Sekvenserbara, GeneralPurpose, Minnesoptimerade.
Standard: Sekvenserbara.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageInMb
Maximal tillåten lagring för en server.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Namnet eller ID:t för ett befintligt undernät eller namnet på ett nytt undernät som ska skapas.
Observera att undernätet kommer att delegeras till Microsoft.DBforPostgreSQL/flexibleServers.
Efter delegering kan det här undernätet inte användas för någon annan typ av Azure-resurser.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetPrefix
Det IP-adressprefix som ska användas när ett nytt vnet skapas i CIDR-format.
Standardvärdet är 10.0.0.0/24.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Det prenumerations-ID som identifierar en Azure-prenumeration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Programspecifika metadata i form av nyckelvärdepar.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Serverversion.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vnet
Namnet eller ID:t för ett befintligt virtuellt nätverk eller namnet på ett nytt nätverk som ska skapas.
Namnet måste vara mellan 2 till 64 tecken.
Namnet måste börja med en bokstav eller ett nummer, sluta med en bokstav, ett nummer eller ett understreck och får bara innehålla bokstäver, siffror, understreck, punkter eller bindestreck.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetPrefix
Det IP-adressprefix som ska användas när ett nytt vnet skapas i CIDR-format.
Standardvärdet är 10.0.0.0/16.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated

## ANTECKNINGAR

ALIAS

## RELATERADE LÄNKAR

