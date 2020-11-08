---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099201"
---
# <span data-ttu-id="676fe-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="676fe-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="676fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="676fe-102">SYNOPSIS</span></span>
<span data-ttu-id="676fe-103">Skapar en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="676fe-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="676fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="676fe-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="676fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="676fe-105">DESCRIPTION</span></span>
<span data-ttu-id="676fe-106">Cmdleten **New-AzureSqlDatabaseServer** skapar en instans av Azure SQL Database Server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="676fe-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="676fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="676fe-107">EXAMPLES</span></span>

### <span data-ttu-id="676fe-108">Exempel 1: skapa en server</span><span class="sxs-lookup"><span data-stu-id="676fe-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="676fe-109">Det här kommandot skapar en version 11-Azure SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="676fe-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="676fe-110">Exempel 2: skapa en server för version 12</span><span class="sxs-lookup"><span data-stu-id="676fe-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="676fe-111">Det här kommandot skapar en version 12-Server.</span><span class="sxs-lookup"><span data-stu-id="676fe-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="676fe-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="676fe-112">PARAMETERS</span></span>

### <span data-ttu-id="676fe-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="676fe-113">-AdministratorLogin</span></span>
<span data-ttu-id="676fe-114">Anger namnet på administratörs kontot för den nya Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="676fe-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

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

### <span data-ttu-id="676fe-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="676fe-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="676fe-116">Anger lösen ordet för administratörs kontot för Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="676fe-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="676fe-117">Du måste ange ett starkt lösen ord.</span><span class="sxs-lookup"><span data-stu-id="676fe-117">You must specify a strong password.</span></span>
<span data-ttu-id="676fe-118">Mer information finns i [starka lösen ord](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) på Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="676fe-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="676fe-119">-Force</span><span class="sxs-lookup"><span data-stu-id="676fe-119">-Force</span></span>
<span data-ttu-id="676fe-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="676fe-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676fe-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="676fe-121">-Location</span></span>
<span data-ttu-id="676fe-122">Anger platsen för data centret där denna cmdlet skapar servern.</span><span class="sxs-lookup"><span data-stu-id="676fe-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="676fe-123">Mer information finns i [Azure-regioner](https://azure.microsoft.com/regions/) ( https://azure.microsoft.com/regions/#services) i Azure-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="676fe-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

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

### <span data-ttu-id="676fe-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="676fe-124">-Profile</span></span>
<span data-ttu-id="676fe-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="676fe-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="676fe-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="676fe-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="676fe-127">-Version</span><span class="sxs-lookup"><span data-stu-id="676fe-127">-Version</span></span>
<span data-ttu-id="676fe-128">Anger versionen för den nya servern.</span><span class="sxs-lookup"><span data-stu-id="676fe-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="676fe-129">Giltiga värden är: 2,0 och 12,0.</span><span class="sxs-lookup"><span data-stu-id="676fe-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676fe-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="676fe-130">-Confirm</span></span>
<span data-ttu-id="676fe-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="676fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="676fe-132">-WhatIf</span></span>
<span data-ttu-id="676fe-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="676fe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="676fe-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="676fe-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="676fe-135">CommonParameters</span></span>
<span data-ttu-id="676fe-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="676fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="676fe-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="676fe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="676fe-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="676fe-138">INPUTS</span></span>

## <span data-ttu-id="676fe-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="676fe-139">OUTPUTS</span></span>

### <span data-ttu-id="676fe-140">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="676fe-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="676fe-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="676fe-141">NOTES</span></span>

## <span data-ttu-id="676fe-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="676fe-142">RELATED LINKS</span></span>

[<span data-ttu-id="676fe-143">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="676fe-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="676fe-144">Skapa server</span><span class="sxs-lookup"><span data-stu-id="676fe-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="676fe-145">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="676fe-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="676fe-146">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="676fe-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="676fe-147">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="676fe-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="676fe-148">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="676fe-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


