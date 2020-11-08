---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099200"
---
# <span data-ttu-id="c0a37-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="c0a37-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="c0a37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0a37-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a37-103">Skapar en server anslutnings kontext.</span><span class="sxs-lookup"><span data-stu-id="c0a37-103">Creates a server connection context.</span></span>

## <span data-ttu-id="c0a37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0a37-104">SYNTAX</span></span>

### <span data-ttu-id="c0a37-105">ByServerNameWithSqlAuth (standard)</span><span class="sxs-lookup"><span data-stu-id="c0a37-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0a37-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="c0a37-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c0a37-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="c0a37-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c0a37-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="c0a37-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c0a37-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="c0a37-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c0a37-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0a37-110">DESCRIPTION</span></span>
<span data-ttu-id="c0a37-111">Cmdleten **New-AzureSqlDatabaseServerContext** skapar en kontext för anslutning till en Azure SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="c0a37-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="c0a37-112">Använd SQL Server-autentisering för att skapa en anslutnings kontext till en SQL-databasserver med hjälp av de angivna autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="c0a37-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="c0a37-113">Du kan ange SQL Server-servern efter namn, efter det fullständiga namnet eller URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="c0a37-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="c0a37-114">För att få en autentiseringsuppgift kan du använda Get-Credential cmdlet som uppmanar dig att ange användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="c0a37-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="c0a37-115">Använd cmdleten **New-AzureSqlDatabaseServerContext** med certifikatbaserad inloggningsautentisering för att skapa en anslutnings kontext till angiven SQL-databasserver med de angivna Azure-prenumerationens data.</span><span class="sxs-lookup"><span data-stu-id="c0a37-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="c0a37-116">Du kan ange SQL-databasserver via namn eller med det fullständigt kvalificerade namnet.</span><span class="sxs-lookup"><span data-stu-id="c0a37-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="c0a37-117">Du kan ange abonnemangs data som en parameter eller kan hämtas från det nuvarande Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c0a37-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="c0a37-118">Använd cmdleten Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx för att välja det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c0a37-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="c0a37-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0a37-119">EXAMPLES</span></span>

### <span data-ttu-id="c0a37-120">Exempel 1: skapa en kontext med SQL Server-identifiering</span><span class="sxs-lookup"><span data-stu-id="c0a37-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="c0a37-121">I det här exemplet används SQL Server-identifieringen.</span><span class="sxs-lookup"><span data-stu-id="c0a37-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="c0a37-122">I det första kommandot uppmanas du att ange Server administratörs uppgifter och autentiseringsuppgifterna lagras i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="c0a37-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="c0a37-123">Det andra kommandot ansluter till SQL-databas servern med namnet lpqd0zbr8y med hjälp av $Credential.</span><span class="sxs-lookup"><span data-stu-id="c0a37-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="c0a37-124">Med kommandot Final skapas en databas som heter Database17 på den server som är en del av kontexten i $Context.</span><span class="sxs-lookup"><span data-stu-id="c0a37-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="c0a37-125">Exempel 2: skapa en kontext med certifikatbaserad inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="c0a37-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="c0a37-126">I det här exemplet används certifikatbaserad lösenordsautentisering.</span><span class="sxs-lookup"><span data-stu-id="c0a37-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="c0a37-127">De två första kommandona tilldelar värden till $SubscriptionId och $Thumbprint variabler.</span><span class="sxs-lookup"><span data-stu-id="c0a37-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="c0a37-128">Det tredje kommandot får certifikatet som identifieras av tumavtrycket i $Thumbprint och lagrar det i $Certificate.</span><span class="sxs-lookup"><span data-stu-id="c0a37-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="c0a37-129">Det fjärde kommandot anger att prenumerationen ska vara Subscription07 och det femte kommandot väljer abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c0a37-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="c0a37-130">Med kommandot slut skapas en kontext i den aktuella prenumerationen för den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c0a37-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c0a37-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0a37-131">PARAMETERS</span></span>

### <span data-ttu-id="c0a37-132">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="c0a37-132">-Credential</span></span>
<span data-ttu-id="c0a37-133">Anger ett objekt som ger SQL Server-autentisering för dig åtkomst till servern.</span><span class="sxs-lookup"><span data-stu-id="c0a37-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a37-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="c0a37-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="c0a37-135">Anger FQDN-namnet (fullkvalificerat domän namn) för Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="c0a37-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="c0a37-136">Till exempel Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="c0a37-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a37-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="c0a37-137">-ManageUrl</span></span>
<span data-ttu-id="c0a37-138">Anger URL-adressen som används för att komma åt DatabaseManagement-portalen för Azure SQL för servern.</span><span class="sxs-lookup"><span data-stu-id="c0a37-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a37-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="c0a37-139">-Profile</span></span>
<span data-ttu-id="c0a37-140">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c0a37-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c0a37-141">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c0a37-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c0a37-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c0a37-142">-ServerName</span></span>
<span data-ttu-id="c0a37-143">Anger namnet på databas servern.</span><span class="sxs-lookup"><span data-stu-id="c0a37-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a37-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c0a37-144">-SubscriptionName</span></span>
<span data-ttu-id="c0a37-145">Anger namnet på den Azure-prenumeration som denna cmdlet använder för att skapa anslutnings kontexten.</span><span class="sxs-lookup"><span data-stu-id="c0a37-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="c0a37-146">Om du inte anger ett värde för denna parameter används den aktuella prenumerationen i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0a37-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="c0a37-147">Kör cmdleten Select-AzureSubscription om du vill ändra det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c0a37-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a37-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="c0a37-148">-UseSubscription</span></span>
<span data-ttu-id="c0a37-149">Anger att denna cmdlet använder Azure-prenumeration för att skapa en anslutnings kontext.</span><span class="sxs-lookup"><span data-stu-id="c0a37-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a37-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a37-150">CommonParameters</span></span>
<span data-ttu-id="c0a37-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0a37-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a37-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a37-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a37-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0a37-153">INPUTS</span></span>

## <span data-ttu-id="c0a37-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0a37-154">OUTPUTS</span></span>

### <span data-ttu-id="c0a37-155">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="c0a37-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="c0a37-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0a37-156">NOTES</span></span>
* <span data-ttu-id="c0a37-157">Om du verifierar utan att ange en domän och om du använder Windows PowerShell 2,0 returnerar Get-Credential cmdleten ett omvänt snedstreck ( \\ ) läggs till till användar namnet, till exempel \user.</span><span class="sxs-lookup"><span data-stu-id="c0a37-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="c0a37-158">Windows PowerShell 3,0 lägger inte till omvända snedstreck.</span><span class="sxs-lookup"><span data-stu-id="c0a37-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="c0a37-159">Det omvända snedstrecket känns inte igen av parametern *Credential* i cmdleten **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="c0a37-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="c0a37-160">Om du vill ta bort den använder du kommandon som ser ut ungefär så här:</span><span class="sxs-lookup"><span data-stu-id="c0a37-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="c0a37-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0a37-161">RELATED LINKS</span></span>

[<span data-ttu-id="c0a37-162">Azure SQL-databas-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c0a37-162">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="c0a37-163">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c0a37-163">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="c0a37-164">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c0a37-164">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="c0a37-165">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c0a37-165">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="c0a37-166">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c0a37-166">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


