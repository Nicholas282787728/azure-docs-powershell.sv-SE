---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410435"
---
# <span data-ttu-id="15bbd-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15bbd-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="15bbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="15bbd-103">Hämtar en Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="15bbd-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="15bbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15bbd-104">SYNTAX</span></span>

### <span data-ttu-id="15bbd-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="15bbd-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15bbd-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15bbd-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15bbd-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15bbd-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15bbd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15bbd-108">DESCRIPTION</span></span>
<span data-ttu-id="15bbd-109">[Den här funktionen är endast tillgänglig för vissa prenumerationer från början.] Cmdleten **Get-AzSynapseSqlDatabase** hämtar information om en Azure SYNAPSE Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="15bbd-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="15bbd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15bbd-110">EXAMPLES</span></span>

### <span data-ttu-id="15bbd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="15bbd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="15bbd-112">Det här kommandot får alla SQL-databaser under en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="15bbd-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="15bbd-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="15bbd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="15bbd-114">Det här kommandot får SQL-databasen under arbets ytans ContosoWorkspace med namnet ContosoSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="15bbd-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="15bbd-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="15bbd-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="15bbd-116">Det här kommandot får alla SQL-databaser under en arbets yta genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="15bbd-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="15bbd-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="15bbd-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="15bbd-118">Det här kommandot får SQL-databasen med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="15bbd-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="15bbd-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15bbd-119">PARAMETERS</span></span>

### <span data-ttu-id="15bbd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bbd-120">-DefaultProfile</span></span>
<span data-ttu-id="15bbd-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15bbd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15bbd-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="15bbd-122">-Name</span></span>
<span data-ttu-id="15bbd-123">Namn på Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="15bbd-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bbd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15bbd-124">-ResourceGroupName</span></span>
<span data-ttu-id="15bbd-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="15bbd-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bbd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15bbd-126">-ResourceId</span></span>
<span data-ttu-id="15bbd-127">Resource-ID för Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="15bbd-127">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bbd-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="15bbd-128">-WorkspaceName</span></span>
<span data-ttu-id="15bbd-129">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="15bbd-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bbd-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="15bbd-130">-WorkspaceObject</span></span>
<span data-ttu-id="15bbd-131">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="15bbd-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15bbd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bbd-132">CommonParameters</span></span>
<span data-ttu-id="15bbd-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15bbd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bbd-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15bbd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bbd-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15bbd-135">INPUTS</span></span>

### <span data-ttu-id="15bbd-136">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="15bbd-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="15bbd-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15bbd-137">OUTPUTS</span></span>

### <span data-ttu-id="15bbd-138">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15bbd-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="15bbd-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15bbd-139">NOTES</span></span>

## <span data-ttu-id="15bbd-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15bbd-140">RELATED LINKS</span></span>
