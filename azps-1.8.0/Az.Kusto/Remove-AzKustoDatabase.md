---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 141c601b5a903462b15bbeb45d410db24608323f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916150"
---
# <span data-ttu-id="6d95e-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="6d95e-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="6d95e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d95e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d95e-103">Tar bort en befintlig Kusto-databas.</span><span class="sxs-lookup"><span data-stu-id="6d95e-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="6d95e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d95e-104">SYNTAX</span></span>

### <span data-ttu-id="6d95e-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="6d95e-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d95e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d95e-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d95e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d95e-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d95e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d95e-108">DESCRIPTION</span></span>
<span data-ttu-id="6d95e-109">Tar bort en befintlig Kusto-databas.</span><span class="sxs-lookup"><span data-stu-id="6d95e-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="6d95e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d95e-110">EXAMPLES</span></span>

### <span data-ttu-id="6d95e-111">Exempel 1 – ta bort en befintlig Kusto-databas efter namn</span><span class="sxs-lookup"><span data-stu-id="6d95e-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="6d95e-112">Kommandot ovan tar bort Kusto-databasen med namnet "mykustodatabase" i klustret "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="6d95e-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="6d95e-113">Exempel 2 – ta bort en befintlig Kusto-databas genom att rör</span><span class="sxs-lookup"><span data-stu-id="6d95e-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="6d95e-114">Ovanstående kommando hämtar Kusto-databasen med namnet "mykustodatabase" i klustret "mykustocluster", som finns i resurs gruppen "testrg" `Get-AzKustoDatabase` , och sedan rör resultatet till `Remove-AzKustoDatabase` för att ta bort den.</span><span class="sxs-lookup"><span data-stu-id="6d95e-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="6d95e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d95e-115">PARAMETERS</span></span>

### <span data-ttu-id="6d95e-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="6d95e-116">-ClusterName</span></span>
<span data-ttu-id="6d95e-117">Namn på det kluster som databasen finns under.</span><span class="sxs-lookup"><span data-stu-id="6d95e-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d95e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d95e-118">-DefaultProfile</span></span>
<span data-ttu-id="6d95e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d95e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d95e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d95e-120">-InputObject</span></span>
<span data-ttu-id="6d95e-121">Kusto.</span><span class="sxs-lookup"><span data-stu-id="6d95e-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d95e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d95e-122">-Name</span></span>
<span data-ttu-id="6d95e-123">Namn på databasen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6d95e-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d95e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d95e-124">-PassThru</span></span>
<span data-ttu-id="6d95e-125">Returnera om den angivna databasen har upphävts eller inte.</span><span class="sxs-lookup"><span data-stu-id="6d95e-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="6d95e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d95e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6d95e-127">Namnet på den resurs grupp som klustret finns under.</span><span class="sxs-lookup"><span data-stu-id="6d95e-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d95e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d95e-128">-ResourceId</span></span>
<span data-ttu-id="6d95e-129">Kusto-databas ResourceID.</span><span class="sxs-lookup"><span data-stu-id="6d95e-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d95e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d95e-130">-Confirm</span></span>
<span data-ttu-id="6d95e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d95e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d95e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d95e-132">-WhatIf</span></span>
<span data-ttu-id="6d95e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d95e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d95e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d95e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d95e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d95e-135">CommonParameters</span></span>
<span data-ttu-id="6d95e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d95e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d95e-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d95e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d95e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d95e-138">INPUTS</span></span>

### <span data-ttu-id="6d95e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6d95e-139">System.String</span></span>

### <span data-ttu-id="6d95e-140">Microsoft. Azure. commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="6d95e-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="6d95e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d95e-141">OUTPUTS</span></span>

### <span data-ttu-id="6d95e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d95e-142">System.Boolean</span></span>

## <span data-ttu-id="6d95e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d95e-143">NOTES</span></span>

## <span data-ttu-id="6d95e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d95e-144">RELATED LINKS</span></span>
