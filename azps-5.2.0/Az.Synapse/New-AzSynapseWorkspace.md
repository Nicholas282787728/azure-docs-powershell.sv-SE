---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397891"
---
# <span data-ttu-id="dd6b8-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd6b8-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="dd6b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6b8-103">Skapar en Synapse för analys.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="dd6b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd6b8-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd6b8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd6b8-105">DESCRIPTION</span></span>
<span data-ttu-id="dd6b8-106">Cmdleten **New-AzSynapseWorkspace** skapar en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="dd6b8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd6b8-107">EXAMPLES</span></span>

### <span data-ttu-id="dd6b8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd6b8-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="dd6b8-109">Det här kommandot skapar en Synapse för analys arbets yta med namnet ContosoWorkspace som använder ContosoAdlGenStorage data lagring i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="dd6b8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd6b8-110">PARAMETERS</span></span>

### <span data-ttu-id="dd6b8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd6b8-111">-AsJob</span></span>
<span data-ttu-id="dd6b8-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dd6b8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd6b8-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dd6b8-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="dd6b8-114">Standard namnet på ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="dd6b8-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="dd6b8-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="dd6b8-116">Standard fil systemet ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="dd6b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6b8-117">-DefaultProfile</span></span>
<span data-ttu-id="dd6b8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd6b8-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="dd6b8-119">-Location</span></span>
<span data-ttu-id="dd6b8-120">Azure-regionen där resursen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="dd6b8-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dd6b8-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="dd6b8-122">Namn på ett Synapse virtuellt nätverk som är dedikerat för Azure Synapse-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b8-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd6b8-123">-Name</span></span>
<span data-ttu-id="dd6b8-124">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd6b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd6b8-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-126">Resource group name.</span></span>

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

### <span data-ttu-id="dd6b8-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="dd6b8-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="dd6b8-128">Autentiseringsuppgifter för SQL-administratör.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b8-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dd6b8-129">-Tag</span></span>
<span data-ttu-id="dd6b8-130">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b8-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd6b8-131">-Confirm</span></span>
<span data-ttu-id="dd6b8-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd6b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd6b8-133">-WhatIf</span></span>
<span data-ttu-id="dd6b8-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd6b8-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd6b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6b8-136">CommonParameters</span></span>
<span data-ttu-id="dd6b8-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6b8-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd6b8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6b8-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd6b8-139">INPUTS</span></span>

### <span data-ttu-id="dd6b8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dd6b8-140">System.String</span></span>

### <span data-ttu-id="dd6b8-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="dd6b8-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dd6b8-142">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="dd6b8-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="dd6b8-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd6b8-143">OUTPUTS</span></span>

### <span data-ttu-id="dd6b8-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd6b8-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dd6b8-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd6b8-145">NOTES</span></span>

## <span data-ttu-id="dd6b8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd6b8-146">RELATED LINKS</span></span>
