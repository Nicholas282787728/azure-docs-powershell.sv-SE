---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099789"
---
# <span data-ttu-id="49882-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="49882-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="49882-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49882-102">SYNOPSIS</span></span>
<span data-ttu-id="49882-103">Får återställnings bara databaser från en angiven server.</span><span class="sxs-lookup"><span data-stu-id="49882-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="49882-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49882-104">SYNTAX</span></span>

### <span data-ttu-id="49882-105">AllDatabasesOnGivenServer (standard)</span><span class="sxs-lookup"><span data-stu-id="49882-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49882-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="49882-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="49882-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="49882-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="49882-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49882-108">DESCRIPTION</span></span>
<span data-ttu-id="49882-109">Cmdleten **Get-AzureSqlRecoverableDatabase** hämtar databaser som går att återskapa från en angiven server.</span><span class="sxs-lookup"><span data-stu-id="49882-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="49882-110">Denna cmdlet hämtar en specifik återställnings bar databas eller alla återställnings bara databaser på en server.</span><span class="sxs-lookup"><span data-stu-id="49882-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="49882-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49882-111">EXAMPLES</span></span>

### <span data-ttu-id="49882-112">Exempel 1: Hämta alla återställnings bara databaser</span><span class="sxs-lookup"><span data-stu-id="49882-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="49882-113">Det här kommandot får alla återställnings bara databaser på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="49882-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="49882-114">Exempel 2: skaffa en specifik återställnings bar databas</span><span class="sxs-lookup"><span data-stu-id="49882-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="49882-115">Med det här kommandot hämtas den databas som heter Database17 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="49882-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="49882-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49882-116">PARAMETERS</span></span>

### <span data-ttu-id="49882-117">-Databas</span><span class="sxs-lookup"><span data-stu-id="49882-117">-Database</span></span>
<span data-ttu-id="49882-118">Anger ett objekt som representerar den återställnings bara databas som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="49882-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49882-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49882-119">-DatabaseName</span></span>
<span data-ttu-id="49882-120">Anger namnet på den återställnings bara databas som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="49882-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49882-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="49882-121">-Profile</span></span>
<span data-ttu-id="49882-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="49882-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49882-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="49882-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49882-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49882-124">-ServerName</span></span>
<span data-ttu-id="49882-125">Anger namnet på den server som den här cmdleten får återställnings bara databaser från.</span><span class="sxs-lookup"><span data-stu-id="49882-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49882-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49882-126">CommonParameters</span></span>
<span data-ttu-id="49882-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49882-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49882-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49882-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49882-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49882-129">INPUTS</span></span>

### <span data-ttu-id="49882-130">Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="49882-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="49882-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49882-131">OUTPUTS</span></span>

### <span data-ttu-id="49882-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="49882-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="49882-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49882-133">NOTES</span></span>
* <span data-ttu-id="49882-134">Du måste använda certifikatbaserad inloggningsautentisering för att köra denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49882-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="49882-135">Kör följande kommandon på den dator där kör denna cmdlet:</span><span class="sxs-lookup"><span data-stu-id="49882-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="49882-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49882-136">RELATED LINKS</span></span>

[<span data-ttu-id="49882-137">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="49882-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="49882-138">Skaffa återställnings bar databas</span><span class="sxs-lookup"><span data-stu-id="49882-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="49882-139">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="49882-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="49882-140">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="49882-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


