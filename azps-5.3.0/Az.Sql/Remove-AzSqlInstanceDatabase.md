---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522200"
---
# <span data-ttu-id="1904c-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1904c-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="1904c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1904c-102">SYNOPSIS</span></span>
<span data-ttu-id="1904c-103">Tar bort en Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="1904c-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="1904c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1904c-104">SYNTAX</span></span>

### <span data-ttu-id="1904c-105">RemoveInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="1904c-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1904c-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="1904c-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1904c-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="1904c-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1904c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1904c-108">DESCRIPTION</span></span>
<span data-ttu-id="1904c-109">Cmdleten **Remove-AzSqlInstanceDatabase** tar bort en Azure SQL-hanterad instans databas.</span><span class="sxs-lookup"><span data-stu-id="1904c-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="1904c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1904c-110">EXAMPLES</span></span>

### <span data-ttu-id="1904c-111">Exempel 1: ta bort en databas från en instans</span><span class="sxs-lookup"><span data-stu-id="1904c-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1904c-112">Det här kommandot tar bort databasen som heter Database01 från instans managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="1904c-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="1904c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1904c-113">PARAMETERS</span></span>

### <span data-ttu-id="1904c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1904c-114">-DefaultProfile</span></span>
<span data-ttu-id="1904c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1904c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1904c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1904c-116">-Force</span></span>
<span data-ttu-id="1904c-117">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="1904c-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1904c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1904c-118">-InputObject</span></span>
<span data-ttu-id="1904c-119">Instans databas objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="1904c-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1904c-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1904c-120">-InstanceName</span></span>
<span data-ttu-id="1904c-121">Instans namnet.</span><span class="sxs-lookup"><span data-stu-id="1904c-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1904c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1904c-122">-Name</span></span>
<span data-ttu-id="1904c-123">Namnet på den Azure SQL instance-databas som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1904c-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1904c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1904c-124">-ResourceGroupName</span></span>
<span data-ttu-id="1904c-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1904c-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1904c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1904c-126">-ResourceId</span></span>
<span data-ttu-id="1904c-127">Resurs-ID för instans databas objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="1904c-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1904c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1904c-128">-Confirm</span></span>
<span data-ttu-id="1904c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1904c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1904c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1904c-130">-WhatIf</span></span>
<span data-ttu-id="1904c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1904c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1904c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1904c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1904c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1904c-133">CommonParameters</span></span>
<span data-ttu-id="1904c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1904c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1904c-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1904c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1904c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1904c-136">INPUTS</span></span>

### <span data-ttu-id="1904c-137">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1904c-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="1904c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1904c-138">System.String</span></span>

## <span data-ttu-id="1904c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1904c-139">OUTPUTS</span></span>

### <span data-ttu-id="1904c-140">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1904c-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="1904c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1904c-141">NOTES</span></span>

## <span data-ttu-id="1904c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1904c-142">RELATED LINKS</span></span>
