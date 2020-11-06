---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a7cf769b1150ef7e209bd02234674bb26927f9a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578751"
---
# <span data-ttu-id="fe7ee-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="fe7ee-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="fe7ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7ee-103">Tar bort granskningen av en databas.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe7ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe7ee-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe7ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe7ee-105">DESCRIPTION</span></span>
<span data-ttu-id="fe7ee-106">Cmdleten **Remove-AzureRmSqlDatabaseAuditing** tar bort granskningen av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="fe7ee-107">Använd den här cmdleten genom att använda parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="fe7ee-108">När du har kört denna cmdlet utförs inte granskning av databasen.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="fe7ee-109">Om kommandot fungerar och du har använt parametern *Passthru* returnerar cmdleten ett objekt som beskriver den aktuella gransknings principen, utöver databasens identifierare.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="fe7ee-110">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>
<span data-ttu-id="fe7ee-111">Om du tar bort granskning av en Azure SQL-databas tas hot identifiering också bort.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>
<span data-ttu-id="fe7ee-112">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fe7ee-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe7ee-113">EXAMPLES</span></span>

### <span data-ttu-id="fe7ee-114">Exempel 1: ta bort granskningen av en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="fe7ee-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fe7ee-115">Det här kommandot tar bort granskningen av databasen som heter Database01.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="fe7ee-116">Databasen finns på Server01, som är tilldelad till resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="fe7ee-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe7ee-117">PARAMETERS</span></span>

### <span data-ttu-id="fe7ee-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe7ee-118">-DatabaseName</span></span>
<span data-ttu-id="fe7ee-119">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fe7ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7ee-120">-DefaultProfile</span></span>
<span data-ttu-id="fe7ee-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fe7ee-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe7ee-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe7ee-122">-PassThru</span></span>
<span data-ttu-id="fe7ee-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-123">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fe7ee-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe7ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe7ee-126">Anger namnet på den resurs grupp som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-126">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="fe7ee-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe7ee-127">-ServerName</span></span>
<span data-ttu-id="fe7ee-128">Anger namnet på den server som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-128">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="fe7ee-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe7ee-129">-Confirm</span></span>
<span data-ttu-id="fe7ee-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe7ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe7ee-131">-WhatIf</span></span>
<span data-ttu-id="fe7ee-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe7ee-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe7ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7ee-134">CommonParameters</span></span>
<span data-ttu-id="fe7ee-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe7ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7ee-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe7ee-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7ee-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe7ee-137">INPUTS</span></span>

### <span data-ttu-id="fe7ee-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fe7ee-138">System.String</span></span>

## <span data-ttu-id="fe7ee-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe7ee-139">OUTPUTS</span></span>

### <span data-ttu-id="fe7ee-140">Microsoft. Azure. commands. SQL. granskning. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fe7ee-140">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="fe7ee-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe7ee-141">NOTES</span></span>

## <span data-ttu-id="fe7ee-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe7ee-142">RELATED LINKS</span></span>

[<span data-ttu-id="fe7ee-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fe7ee-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="fe7ee-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fe7ee-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="fe7ee-145">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fe7ee-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


