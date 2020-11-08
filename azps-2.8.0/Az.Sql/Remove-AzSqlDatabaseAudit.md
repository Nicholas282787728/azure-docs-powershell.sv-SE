---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: ad0103e2a4d529a4f306749a1d55ca0b6eadc013
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920558"
---
# <span data-ttu-id="112fe-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="112fe-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="112fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="112fe-102">SYNOPSIS</span></span>
<span data-ttu-id="112fe-103">Tar bort gransknings inställningar för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="112fe-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="112fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="112fe-104">SYNTAX</span></span>

### <span data-ttu-id="112fe-105">DatabaseParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="112fe-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="112fe-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="112fe-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="112fe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="112fe-107">DESCRIPTION</span></span>
<span data-ttu-id="112fe-108">Cmdleten **Remove-AzSqlDatabaseAudit** tar bort gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="112fe-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="112fe-109">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="112fe-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="112fe-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="112fe-110">EXAMPLES</span></span>

### <span data-ttu-id="112fe-111">Exempel 1: ta bort gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="112fe-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="112fe-112">Exempel 2: ta bort och granska gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="112fe-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="112fe-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="112fe-113">PARAMETERS</span></span>

### <span data-ttu-id="112fe-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="112fe-114">-DatabaseName</span></span>
<span data-ttu-id="112fe-115">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="112fe-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112fe-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="112fe-116">-DatabaseObject</span></span>
<span data-ttu-id="112fe-117">Databasobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="112fe-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="112fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112fe-118">-DefaultProfile</span></span>
<span data-ttu-id="112fe-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="112fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="112fe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="112fe-120">-ResourceGroupName</span></span>
<span data-ttu-id="112fe-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="112fe-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112fe-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="112fe-122">-ServerName</span></span>
<span data-ttu-id="112fe-123">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="112fe-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112fe-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="112fe-124">-Confirm</span></span>
<span data-ttu-id="112fe-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="112fe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="112fe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="112fe-126">-WhatIf</span></span>
<span data-ttu-id="112fe-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="112fe-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="112fe-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="112fe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="112fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112fe-129">CommonParameters</span></span>
<span data-ttu-id="112fe-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="112fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112fe-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="112fe-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112fe-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="112fe-132">INPUTS</span></span>

### <span data-ttu-id="112fe-133">System. String</span><span class="sxs-lookup"><span data-stu-id="112fe-133">System.String</span></span>

### <span data-ttu-id="112fe-134">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="112fe-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="112fe-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="112fe-135">OUTPUTS</span></span>

### <span data-ttu-id="112fe-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="112fe-136">System.Boolean</span></span>

## <span data-ttu-id="112fe-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="112fe-137">NOTES</span></span>

## <span data-ttu-id="112fe-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="112fe-138">RELATED LINKS</span></span>