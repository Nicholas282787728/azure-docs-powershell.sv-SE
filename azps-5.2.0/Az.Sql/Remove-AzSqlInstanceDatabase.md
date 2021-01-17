---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416280"
---
# <span data-ttu-id="eb912-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eb912-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="eb912-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb912-102">SYNOPSIS</span></span>
<span data-ttu-id="eb912-103">Tar bort en Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="eb912-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="eb912-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb912-104">SYNTAX</span></span>

### <span data-ttu-id="eb912-105">RemoveInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="eb912-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb912-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="eb912-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb912-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="eb912-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb912-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb912-108">DESCRIPTION</span></span>
<span data-ttu-id="eb912-109">Cmdleten **Remove-AzSqlInstanceDatabase** tar bort en Azure SQL-hanterad instans databas.</span><span class="sxs-lookup"><span data-stu-id="eb912-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="eb912-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb912-110">EXAMPLES</span></span>

### <span data-ttu-id="eb912-111">Exempel 1: ta bort en databas från en instans</span><span class="sxs-lookup"><span data-stu-id="eb912-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eb912-112">Det här kommandot tar bort databasen som heter Database01 från instans managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="eb912-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="eb912-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb912-113">PARAMETERS</span></span>

### <span data-ttu-id="eb912-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb912-114">-DefaultProfile</span></span>
<span data-ttu-id="eb912-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb912-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb912-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eb912-116">-Force</span></span>
<span data-ttu-id="eb912-117">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="eb912-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="eb912-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb912-118">-InputObject</span></span>
<span data-ttu-id="eb912-119">Instans databas objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="eb912-119">The Instance Database object to remove</span></span>

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

### <span data-ttu-id="eb912-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="eb912-120">-InstanceName</span></span>
<span data-ttu-id="eb912-121">Instans namnet.</span><span class="sxs-lookup"><span data-stu-id="eb912-121">The instance name.</span></span>

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

### <span data-ttu-id="eb912-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb912-122">-Name</span></span>
<span data-ttu-id="eb912-123">Namnet på den Azure SQL instance-databas som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="eb912-123">The name of the Azure SQL Instance Database to remove.</span></span>

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

### <span data-ttu-id="eb912-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb912-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb912-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb912-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb912-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb912-126">-ResourceId</span></span>
<span data-ttu-id="eb912-127">Resurs-ID för instans databas objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="eb912-127">The resource id of Instance Database object to remove</span></span>

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

### <span data-ttu-id="eb912-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb912-128">-Confirm</span></span>
<span data-ttu-id="eb912-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb912-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb912-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb912-130">-WhatIf</span></span>
<span data-ttu-id="eb912-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb912-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb912-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb912-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb912-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb912-133">CommonParameters</span></span>
<span data-ttu-id="eb912-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb912-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb912-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb912-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb912-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb912-136">INPUTS</span></span>

### <span data-ttu-id="eb912-137">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="eb912-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="eb912-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eb912-138">System.String</span></span>

## <span data-ttu-id="eb912-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb912-139">OUTPUTS</span></span>

### <span data-ttu-id="eb912-140">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="eb912-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="eb912-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb912-141">NOTES</span></span>

## <span data-ttu-id="eb912-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb912-142">RELATED LINKS</span></span>
