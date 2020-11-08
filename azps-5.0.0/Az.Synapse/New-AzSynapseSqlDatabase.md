---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 16f2df5900fcc522f0ff3afb7b9f5b14ea5f0b64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272523"
---
# <span data-ttu-id="d2318-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d2318-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="d2318-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2318-102">SYNOPSIS</span></span>
<span data-ttu-id="d2318-103">Skapar en Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="d2318-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d2318-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2318-104">SYNTAX</span></span>

### <span data-ttu-id="d2318-105">CreateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d2318-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2318-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2318-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2318-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2318-107">DESCRIPTION</span></span>
<span data-ttu-id="d2318-108">Cmdleten **Get-AzSynapseSqlDatabase** hämtar information om en Azure SYNAPSE Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="d2318-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="d2318-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2318-109">EXAMPLES</span></span>

### <span data-ttu-id="d2318-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d2318-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase 
```

<span data-ttu-id="d2318-111">Det här kommandot skapar en Azure Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="d2318-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d2318-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2318-112">PARAMETERS</span></span>

### <span data-ttu-id="d2318-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2318-113">-AsJob</span></span>
<span data-ttu-id="d2318-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d2318-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2318-115">-Sortering</span><span class="sxs-lookup"><span data-stu-id="d2318-115">-Collation</span></span>
<span data-ttu-id="d2318-116">Sortering definierar regler som sorterar och jämför data och kan inte ändras efter att SQL-poolen har skapats.</span><span class="sxs-lookup"><span data-stu-id="d2318-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="d2318-117">Standard sorteringen är SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="d2318-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="d2318-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2318-118">-DefaultProfile</span></span>
<span data-ttu-id="d2318-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2318-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2318-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="d2318-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="d2318-121">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="d2318-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2318-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2318-122">-Name</span></span>
<span data-ttu-id="d2318-123">Namn på Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="d2318-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2318-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2318-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2318-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d2318-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2318-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d2318-126">-Tag</span></span>
<span data-ttu-id="d2318-127">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="d2318-127">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2318-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2318-128">-WorkspaceName</span></span>
<span data-ttu-id="d2318-129">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d2318-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2318-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d2318-130">-WorkspaceObject</span></span>
<span data-ttu-id="d2318-131">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2318-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2318-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2318-132">-Confirm</span></span>
<span data-ttu-id="d2318-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2318-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2318-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2318-134">-WhatIf</span></span>
<span data-ttu-id="d2318-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2318-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2318-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2318-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2318-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2318-137">CommonParameters</span></span>
<span data-ttu-id="d2318-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2318-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2318-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2318-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2318-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2318-140">INPUTS</span></span>

### <span data-ttu-id="d2318-141">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2318-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d2318-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2318-142">OUTPUTS</span></span>

### <span data-ttu-id="d2318-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d2318-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="d2318-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2318-144">NOTES</span></span>

## <span data-ttu-id="d2318-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2318-145">RELATED LINKS</span></span>
