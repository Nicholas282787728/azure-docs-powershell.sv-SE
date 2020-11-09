---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320388"
---
# <span data-ttu-id="c5e92-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c5e92-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="c5e92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5e92-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e92-103">Stoppar en aktivitet i Azure Database migration service som körs.</span><span class="sxs-lookup"><span data-stu-id="c5e92-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="c5e92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5e92-104">SYNTAX</span></span>

### <span data-ttu-id="c5e92-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c5e92-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e92-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5e92-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e92-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5e92-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e92-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5e92-108">DESCRIPTION</span></span>
<span data-ttu-id="c5e92-109">Stop-AzDataMigrationTask cmdlet stoppar databas flyttnings aktivitet i kör tillstånd.</span><span class="sxs-lookup"><span data-stu-id="c5e92-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="c5e92-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5e92-110">EXAMPLES</span></span>

### <span data-ttu-id="c5e92-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c5e92-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="c5e92-112">Ovan exemplet ovan stoppar Azure Database migration service-uppgift med namnet myDMSTask associerat med Project myDMSProject och instans för Azure Database migration service med namnet TestService</span><span class="sxs-lookup"><span data-stu-id="c5e92-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="c5e92-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c5e92-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="c5e92-114">Ovan exemplet ovan stoppar Azure Database migration service-uppgift som skickades som indataparameter PSProjectTask-objekt</span><span class="sxs-lookup"><span data-stu-id="c5e92-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="c5e92-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5e92-115">PARAMETERS</span></span>

### <span data-ttu-id="c5e92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e92-116">-DefaultProfile</span></span>
<span data-ttu-id="c5e92-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5e92-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5e92-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5e92-118">-InputObject</span></span>
<span data-ttu-id="c5e92-119">PSProjectTask-objekt.</span><span class="sxs-lookup"><span data-stu-id="c5e92-119">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e92-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c5e92-120">-Name</span></span>
<span data-ttu-id="c5e92-121">Uppgiftens namn.</span><span class="sxs-lookup"><span data-stu-id="c5e92-121">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e92-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5e92-122">-PassThru</span></span>
<span data-ttu-id="c5e92-123">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="c5e92-123">Returns an true/false.</span></span>
<span data-ttu-id="c5e92-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c5e92-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c5e92-125">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="c5e92-125">-ProjectName</span></span>
<span data-ttu-id="c5e92-126">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="c5e92-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e92-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e92-127">-ResourceGroupName</span></span>
<span data-ttu-id="c5e92-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c5e92-128">The name of the resource group .</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e92-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5e92-129">-ResourceId</span></span>
<span data-ttu-id="c5e92-130">ProjectTask resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c5e92-130">ProjectTask Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e92-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c5e92-131">-ServiceName</span></span>
<span data-ttu-id="c5e92-132">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="c5e92-132">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e92-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5e92-133">-Confirm</span></span>
<span data-ttu-id="c5e92-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5e92-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e92-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e92-135">-WhatIf</span></span>
<span data-ttu-id="c5e92-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c5e92-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e92-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c5e92-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e92-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e92-138">CommonParameters</span></span>
<span data-ttu-id="c5e92-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e92-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e92-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e92-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e92-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5e92-141">INPUTS</span></span>

### <span data-ttu-id="c5e92-142">Microsoft. Azure. commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="c5e92-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="c5e92-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c5e92-143">System.String</span></span>

## <span data-ttu-id="c5e92-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5e92-144">OUTPUTS</span></span>

### <span data-ttu-id="c5e92-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5e92-145">System.Boolean</span></span>

## <span data-ttu-id="c5e92-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5e92-146">NOTES</span></span>

## <span data-ttu-id="c5e92-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5e92-147">RELATED LINKS</span></span>
