---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 6bb2a3891abe8453ee8460f6879dbc134f6ab29b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920398"
---
# <span data-ttu-id="fedae-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="fedae-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="fedae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fedae-102">SYNOPSIS</span></span>
<span data-ttu-id="fedae-103">Hämtar Länkar för geo-replikering mellan en Azure SQL-databas och en resurs grupp eller SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fedae-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="fedae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fedae-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fedae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fedae-105">DESCRIPTION</span></span>
<span data-ttu-id="fedae-106">Cmdleten **Get-AzSqlDatabaseReplicationLink** ersätter cmdleten **Get-AzSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="fedae-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="fedae-107">Den får alla geo-replikeringslänken-länkar mellan den angivna Azure SQL-databasen och en resurs grupp eller en AzureSQL-Server.</span><span class="sxs-lookup"><span data-stu-id="fedae-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="fedae-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fedae-108">EXAMPLES</span></span>

## <span data-ttu-id="fedae-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fedae-109">PARAMETERS</span></span>

### <span data-ttu-id="fedae-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fedae-110">-DatabaseName</span></span>
<span data-ttu-id="fedae-111">Anger namnet på den SQL-databas som du vill hämta länkar för.</span><span class="sxs-lookup"><span data-stu-id="fedae-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fedae-112">-DefaultProfile</span></span>
<span data-ttu-id="fedae-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fedae-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fedae-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fedae-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="fedae-115">Anger namnet på den resurs grupp som partnern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="fedae-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedae-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="fedae-116">-PartnerServerName</span></span>
<span data-ttu-id="fedae-117">Anger namnet på partnerns Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fedae-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="fedae-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fedae-118">-ResourceGroupName</span></span>
<span data-ttu-id="fedae-119">Anger namnet på den databas som du vill hämta länkar för.</span><span class="sxs-lookup"><span data-stu-id="fedae-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedae-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fedae-120">-ServerName</span></span>
<span data-ttu-id="fedae-121">Anger namnet på SQL Server för databasen där länkar ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="fedae-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedae-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fedae-122">-Confirm</span></span>
<span data-ttu-id="fedae-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fedae-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fedae-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fedae-124">-WhatIf</span></span>
<span data-ttu-id="fedae-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fedae-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fedae-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fedae-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fedae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedae-127">CommonParameters</span></span>
<span data-ttu-id="fedae-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fedae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedae-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fedae-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedae-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fedae-130">INPUTS</span></span>

### <span data-ttu-id="fedae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fedae-131">System.String</span></span>

## <span data-ttu-id="fedae-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fedae-132">OUTPUTS</span></span>

### <span data-ttu-id="fedae-133">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="fedae-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="fedae-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fedae-134">NOTES</span></span>

## <span data-ttu-id="fedae-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fedae-135">RELATED LINKS</span></span>

[<span data-ttu-id="fedae-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fedae-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
