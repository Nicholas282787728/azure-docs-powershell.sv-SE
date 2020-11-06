---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 993d7ef8958e96cebcd104d25550e860cdfd1853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581636"
---
# <span data-ttu-id="ee151-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="ee151-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="ee151-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee151-102">SYNOPSIS</span></span>
<span data-ttu-id="ee151-103">Hämtar Länkar för geo-replikering mellan en Azure SQL-databas och en resurs grupp eller SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ee151-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee151-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee151-104">SYNTAX</span></span>

### <span data-ttu-id="ee151-105">ByDatabaseName (standard)</span><span class="sxs-lookup"><span data-stu-id="ee151-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee151-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ee151-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee151-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee151-107">DESCRIPTION</span></span>
<span data-ttu-id="ee151-108">Cmdleten **Get-AzureRMSqlDatabaseReplicationLink** ersätter cmdleten **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="ee151-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="ee151-109">Den får alla geo-replikeringslänken-länkar mellan den angivna Azure SQL-databasen och en resurs grupp eller en AzureSQL-Server.</span><span class="sxs-lookup"><span data-stu-id="ee151-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="ee151-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee151-110">EXAMPLES</span></span>

## <span data-ttu-id="ee151-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee151-111">PARAMETERS</span></span>

### <span data-ttu-id="ee151-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee151-112">-DatabaseName</span></span>
<span data-ttu-id="ee151-113">Anger namnet på den SQL-databas som du vill hämta länkar för.</span><span class="sxs-lookup"><span data-stu-id="ee151-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="ee151-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee151-114">-DefaultProfile</span></span>
<span data-ttu-id="ee151-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ee151-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee151-116">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee151-116">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ee151-117">Anger namnet på den resurs grupp som partnern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="ee151-117">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="ee151-118">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ee151-118">-PartnerServerName</span></span>
<span data-ttu-id="ee151-119">Anger namnet på partnerns Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ee151-119">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee151-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee151-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee151-121">Anger namnet på den databas som du vill hämta länkar för.</span><span class="sxs-lookup"><span data-stu-id="ee151-121">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="ee151-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ee151-122">-ServerName</span></span>
<span data-ttu-id="ee151-123">Anger namnet på SQL Server för databasen där länkar ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="ee151-123">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="ee151-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee151-124">-Confirm</span></span>
<span data-ttu-id="ee151-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee151-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee151-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee151-126">-WhatIf</span></span>
<span data-ttu-id="ee151-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee151-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee151-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee151-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee151-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee151-129">CommonParameters</span></span>
<span data-ttu-id="ee151-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee151-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee151-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee151-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee151-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee151-132">INPUTS</span></span>

### <span data-ttu-id="ee151-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ee151-133">System.String</span></span>

## <span data-ttu-id="ee151-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee151-134">OUTPUTS</span></span>

### <span data-ttu-id="ee151-135">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ee151-135">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="ee151-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee151-136">NOTES</span></span>

## <span data-ttu-id="ee151-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee151-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee151-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ee151-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
