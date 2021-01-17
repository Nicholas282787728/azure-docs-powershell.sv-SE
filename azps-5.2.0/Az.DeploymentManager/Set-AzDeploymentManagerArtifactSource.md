---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393536"
---
# <span data-ttu-id="09c1d-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="09c1d-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="09c1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="09c1d-103">Uppdaterar källan för artefakter.</span><span class="sxs-lookup"><span data-stu-id="09c1d-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="09c1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09c1d-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09c1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="09c1d-106">Cmdleten **set-AzDeploymentManagerArtifactSource** uppdaterar en artefakt källa med angivet artefakt objekt.</span><span class="sxs-lookup"><span data-stu-id="09c1d-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="09c1d-107">Cmdleten returnerar det uppdaterade ArtifactSource-objektet.</span><span class="sxs-lookup"><span data-stu-id="09c1d-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="09c1d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09c1d-108">EXAMPLES</span></span>

### <span data-ttu-id="09c1d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="09c1d-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="09c1d-110">Det här kommandot uppdaterar en artefakt källa vars namn och ResourceGroup matchar $artifactSourceObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="09c1d-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="09c1d-111">Artefakt källan uppdaterades till de egenskaper som angavs i $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="09c1d-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="09c1d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09c1d-112">PARAMETERS</span></span>

### <span data-ttu-id="09c1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c1d-113">-DefaultProfile</span></span>
<span data-ttu-id="09c1d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09c1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09c1d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09c1d-115">-InputObject</span></span>
<span data-ttu-id="09c1d-116">Objektet artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="09c1d-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09c1d-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09c1d-117">-Confirm</span></span>
<span data-ttu-id="09c1d-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09c1d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c1d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c1d-119">-WhatIf</span></span>
<span data-ttu-id="09c1d-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09c1d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09c1d-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09c1d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c1d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c1d-122">CommonParameters</span></span>
<span data-ttu-id="09c1d-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c1d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c1d-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09c1d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c1d-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09c1d-125">INPUTS</span></span>

### <span data-ttu-id="09c1d-126">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="09c1d-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="09c1d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09c1d-127">OUTPUTS</span></span>

### <span data-ttu-id="09c1d-128">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="09c1d-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="09c1d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09c1d-129">NOTES</span></span>

## <span data-ttu-id="09c1d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09c1d-130">RELATED LINKS</span></span>
