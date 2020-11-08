---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093296"
---
# <span data-ttu-id="e3079-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="e3079-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="e3079-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3079-102">SYNOPSIS</span></span>
<span data-ttu-id="e3079-103">Hämtar kvot information för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="e3079-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="e3079-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3079-104">SYNTAX</span></span>

### <span data-ttu-id="e3079-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="e3079-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e3079-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="e3079-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3079-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3079-107">DESCRIPTION</span></span>
<span data-ttu-id="e3079-108">Cmdleten **Get-AzureSqlDatabaseServerQuota** hämtar kvot informationen för en viss instans av Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="e3079-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="e3079-109">Ange en anslutnings kontext eller Server namnet.</span><span class="sxs-lookup"><span data-stu-id="e3079-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="e3079-110">Om du inte anger ett kvot namn får denna cmdlet all kvot information för servern.</span><span class="sxs-lookup"><span data-stu-id="e3079-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="e3079-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3079-111">EXAMPLES</span></span>

### <span data-ttu-id="e3079-112">Exempel 1: Hämta information för en specifik kvot</span><span class="sxs-lookup"><span data-stu-id="e3079-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="e3079-113">Med det här kommandot får du den kvot som heter Premium_Databases från den Azure SQL-databasserver som anges av anslutningen som lagras i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="e3079-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="e3079-114">Exempel 2: Hämta information för alla kvoter</span><span class="sxs-lookup"><span data-stu-id="e3079-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="e3079-115">Det här kommandot får alla kvot värden från den server som anges av anslutnings $Context.</span><span class="sxs-lookup"><span data-stu-id="e3079-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="e3079-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3079-116">PARAMETERS</span></span>

### <span data-ttu-id="e3079-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="e3079-117">-ConnectionContext</span></span>
<span data-ttu-id="e3079-118">Anger en servers anslutning.</span><span class="sxs-lookup"><span data-stu-id="e3079-118">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3079-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="e3079-119">-Profile</span></span>
<span data-ttu-id="e3079-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e3079-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3079-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e3079-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3079-122">-QuotaName</span><span class="sxs-lookup"><span data-stu-id="e3079-122">-QuotaName</span></span>
<span data-ttu-id="e3079-123">Anger namnet på det kvot värde som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="e3079-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3079-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e3079-124">-ServerName</span></span>
<span data-ttu-id="e3079-125">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="e3079-125">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3079-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3079-126">CommonParameters</span></span>
<span data-ttu-id="e3079-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3079-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3079-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3079-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3079-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3079-129">INPUTS</span></span>

## <span data-ttu-id="e3079-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3079-130">OUTPUTS</span></span>

### <span data-ttu-id="e3079-131">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. ServerQuota []</span><span class="sxs-lookup"><span data-stu-id="e3079-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="e3079-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3079-132">NOTES</span></span>
* <span data-ttu-id="e3079-133">Verifiera: denna cmdlet kan använda SQL Server-serverautentisering eller certifikatbaserad identifiering.</span><span class="sxs-lookup"><span data-stu-id="e3079-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="e3079-134">Exempel på hur du konfigurerar en konfiguration finns i New-AzureSqlDatabaseServerContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3079-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="e3079-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3079-135">RELATED LINKS</span></span>

[<span data-ttu-id="e3079-136">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="e3079-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e3079-137">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e3079-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e3079-138">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="e3079-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


