---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 2bf632e0135031a9bc2454ac200cbe7aa40bef3c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089263"
---
# <span data-ttu-id="68ef0-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="68ef0-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="68ef0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="68ef0-103">Hämtar Länkar för geo-replikering mellan en Azure SQL-databas och en resurs grupp eller SQL Server.</span><span class="sxs-lookup"><span data-stu-id="68ef0-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="68ef0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68ef0-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ef0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="68ef0-106">Cmdleten **Get-AzSqlDatabaseReplicationLink** ersätter cmdleten **Get-AzSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="68ef0-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="68ef0-107">Den får alla geo-replikeringslänken-länkar mellan den angivna Azure SQL-databasen och en resurs grupp eller en AzureSQL-Server.</span><span class="sxs-lookup"><span data-stu-id="68ef0-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="68ef0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68ef0-108">EXAMPLES</span></span>

## <span data-ttu-id="68ef0-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68ef0-109">PARAMETERS</span></span>

### <span data-ttu-id="68ef0-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="68ef0-110">-DatabaseName</span></span>
<span data-ttu-id="68ef0-111">Anger namnet på den SQL-databas som du vill hämta länkar för.</span><span class="sxs-lookup"><span data-stu-id="68ef0-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="68ef0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ef0-112">-DefaultProfile</span></span>
<span data-ttu-id="68ef0-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="68ef0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68ef0-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ef0-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="68ef0-115">Anger namnet på den resurs grupp som partnern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="68ef0-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="68ef0-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="68ef0-116">-PartnerServerName</span></span>
<span data-ttu-id="68ef0-117">Anger namnet på partnerns Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="68ef0-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

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

### <span data-ttu-id="68ef0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ef0-118">-ResourceGroupName</span></span>
<span data-ttu-id="68ef0-119">Anger namnet på den databas som du vill hämta länkar för.</span><span class="sxs-lookup"><span data-stu-id="68ef0-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="68ef0-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68ef0-120">-ServerName</span></span>
<span data-ttu-id="68ef0-121">Anger namnet på SQL Server för databasen där länkar ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="68ef0-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="68ef0-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68ef0-122">-Confirm</span></span>
<span data-ttu-id="68ef0-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68ef0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ef0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ef0-124">-WhatIf</span></span>
<span data-ttu-id="68ef0-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68ef0-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68ef0-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68ef0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ef0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ef0-127">CommonParameters</span></span>
<span data-ttu-id="68ef0-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ef0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ef0-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68ef0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ef0-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68ef0-130">INPUTS</span></span>

### <span data-ttu-id="68ef0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="68ef0-131">System.String</span></span>

## <span data-ttu-id="68ef0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68ef0-132">OUTPUTS</span></span>

### <span data-ttu-id="68ef0-133">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="68ef0-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="68ef0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68ef0-134">NOTES</span></span>

## <span data-ttu-id="68ef0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68ef0-135">RELATED LINKS</span></span>

[<span data-ttu-id="68ef0-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="68ef0-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
