---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093294"
---
# <span data-ttu-id="08284-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="08284-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="08284-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08284-102">SYNOPSIS</span></span>
<span data-ttu-id="08284-103">Hämtar tjänste mål för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="08284-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="08284-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08284-104">SYNTAX</span></span>

### <span data-ttu-id="08284-105">ByConnectionContext (standard)</span><span class="sxs-lookup"><span data-stu-id="08284-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="08284-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="08284-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="08284-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08284-107">DESCRIPTION</span></span>
<span data-ttu-id="08284-108">Cmdleten **Get-AzureSqlDatabaseServiceObjective** hämtar tjänst mål för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="08284-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="08284-109">Tjänste mål kallas prestanda nivåer.</span><span class="sxs-lookup"><span data-stu-id="08284-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="08284-110">Om du inte anger något tjänst mål returnerar denna cmdlet alla giltiga tjänst mål för den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="08284-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="08284-111">Denna cmdlet gäller för grundläggande, standard-och premie tjänst nivåer.</span><span class="sxs-lookup"><span data-stu-id="08284-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="08284-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08284-112">EXAMPLES</span></span>

### <span data-ttu-id="08284-113">Exempel 1: få alla tjänst mål genom att använda en kontext för anslutning</span><span class="sxs-lookup"><span data-stu-id="08284-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="08284-114">Det här kommandot får alla tjänst mål för servern som kontexten för anslutning $Context anger.</span><span class="sxs-lookup"><span data-stu-id="08284-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="08284-115">Exempel 2: få alla tjänst mål genom att använda ett server namn</span><span class="sxs-lookup"><span data-stu-id="08284-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="08284-116">Det här kommandot får alla tjänst mål för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="08284-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="08284-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08284-117">PARAMETERS</span></span>

### <span data-ttu-id="08284-118">-Kontext</span><span class="sxs-lookup"><span data-stu-id="08284-118">-Context</span></span>
<span data-ttu-id="08284-119">Anger en servers anslutning.</span><span class="sxs-lookup"><span data-stu-id="08284-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08284-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="08284-120">-Profile</span></span>
<span data-ttu-id="08284-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="08284-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08284-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="08284-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08284-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08284-123">-ServerName</span></span>
<span data-ttu-id="08284-124">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="08284-124">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="08284-125">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="08284-125">-ServiceObjective</span></span>
<span data-ttu-id="08284-126">Anger ett objekt som representerar det tjänst mål som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="08284-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="08284-127">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="08284-127">Valid values are:</span></span> 

- <span data-ttu-id="08284-128">Grundläggande: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="08284-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="08284-129">Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="08284-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="08284-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="08284-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="08284-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="08284-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="08284-132">\* Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="08284-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="08284-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="08284-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="08284-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="08284-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="08284-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="08284-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="08284-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="08284-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="08284-137">\* Standard (S3) är en del av den senaste SQL-V12 (för hands version).</span><span class="sxs-lookup"><span data-stu-id="08284-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="08284-138">Mer information finns i [Nyheter i för hands versionen av V12 för Azure SQL Database](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) i Azure-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="08284-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08284-139">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="08284-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="08284-140">Anger namnet på ett tjänst mål som ska visas.</span><span class="sxs-lookup"><span data-stu-id="08284-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="08284-141">Giltiga värden är: Basic, S0, S1, S2, S3, P1, P2 och P3.</span><span class="sxs-lookup"><span data-stu-id="08284-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="08284-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08284-142">CommonParameters</span></span>
<span data-ttu-id="08284-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08284-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08284-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08284-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08284-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08284-145">INPUTS</span></span>

### <span data-ttu-id="08284-146">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="08284-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="08284-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08284-147">OUTPUTS</span></span>

### <span data-ttu-id="08284-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="08284-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="08284-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08284-149">NOTES</span></span>

## <span data-ttu-id="08284-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08284-150">RELATED LINKS</span></span>

[<span data-ttu-id="08284-151">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="08284-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="08284-152">Skaffa service nivå mål</span><span class="sxs-lookup"><span data-stu-id="08284-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="08284-153">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="08284-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="08284-154">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="08284-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


