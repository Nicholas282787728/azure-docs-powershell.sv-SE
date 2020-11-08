---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 9ff2284e602fe0bb9a7afea886385a02f89298a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920417"
---
# <span data-ttu-id="4b9a1-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="4b9a1-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="4b9a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9a1-103">Hämtar en databas och dess utökade egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="4b9a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b9a1-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b9a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="4b9a1-106">Cmdleten **Get-AzSqlDatabaseExpanded** hämtar en databas och dess utökade egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="4b9a1-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4b9a1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b9a1-108">EXAMPLES</span></span>

### <span data-ttu-id="4b9a1-109">Exempel 1: Hämta databas objekt med information om tjänst nivå klassificering</span><span class="sxs-lookup"><span data-stu-id="4b9a1-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4b9a1-110">Det här kommandot returnerar den databas som har utökade egenskaper som innehåller information om tjänst nivå klassificering.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="4b9a1-111">Exempel 2: lista databas objekt med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="4b9a1-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="4b9a1-112">Det här kommandot returnerar utökade databasobjektet för alla databaser i Server01 som börjar med "databas".</span><span class="sxs-lookup"><span data-stu-id="4b9a1-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="4b9a1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b9a1-113">PARAMETERS</span></span>

### <span data-ttu-id="4b9a1-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b9a1-114">-DatabaseName</span></span>
<span data-ttu-id="4b9a1-115">Anger namnet på den databas som ska visas.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4b9a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b9a1-116">-DefaultProfile</span></span>
<span data-ttu-id="4b9a1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4b9a1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b9a1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b9a1-118">-ResourceGroupName</span></span>
<span data-ttu-id="4b9a1-119">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4b9a1-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4b9a1-120">-ServerName</span></span>
<span data-ttu-id="4b9a1-121">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4b9a1-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b9a1-122">-Confirm</span></span>
<span data-ttu-id="4b9a1-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b9a1-124">-WhatIf</span></span>
<span data-ttu-id="4b9a1-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b9a1-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9a1-127">CommonParameters</span></span>
<span data-ttu-id="4b9a1-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9a1-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b9a1-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9a1-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b9a1-130">INPUTS</span></span>

### <span data-ttu-id="4b9a1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4b9a1-131">System.String</span></span>

## <span data-ttu-id="4b9a1-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b9a1-132">OUTPUTS</span></span>

### <span data-ttu-id="4b9a1-133">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="4b9a1-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="4b9a1-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b9a1-134">NOTES</span></span>

## <span data-ttu-id="4b9a1-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b9a1-135">RELATED LINKS</span></span>

[<span data-ttu-id="4b9a1-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4b9a1-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)