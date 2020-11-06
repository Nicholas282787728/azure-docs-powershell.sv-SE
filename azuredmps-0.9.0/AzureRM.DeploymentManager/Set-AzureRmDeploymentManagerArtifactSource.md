---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571684"
---
# <span data-ttu-id="6a9f2-101">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6a9f2-101">Set-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="6a9f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9f2-103">Uppdaterar en artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-103">Updates an artifact source.</span></span>

## <span data-ttu-id="6a9f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a9f2-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a9f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a9f2-105">DESCRIPTION</span></span>
<span data-ttu-id="6a9f2-106">Cmdleten **set-AzureRmDeploymentManagerArtifactSource** uppdaterar en artefakt källa med angivet artefakt objekt.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-106">The **Set-AzureRmDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="6a9f2-107">Cmdleten returnerar det uppdaterade ArtifactSource-objektet.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="6a9f2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a9f2-108">EXAMPLES</span></span>

### <span data-ttu-id="6a9f2-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6a9f2-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="6a9f2-110">Det här kommandot uppdaterar en artefakt källa vars namn och ResourceGroup matchar $artifactSourceObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="6a9f2-111">Artefakt källan uppdaterades till de egenskaper som angavs i $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="6a9f2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a9f2-112">PARAMETERS</span></span>

### <span data-ttu-id="6a9f2-113">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6a9f2-113">-ArtifactSource</span></span>
<span data-ttu-id="6a9f2-114">Objektet artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-114">The artifact source object.</span></span>

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

### <span data-ttu-id="6a9f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9f2-115">-DefaultProfile</span></span>
<span data-ttu-id="6a9f2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a9f2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a9f2-117">-Confirm</span></span>
<span data-ttu-id="6a9f2-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a9f2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a9f2-119">-WhatIf</span></span>
<span data-ttu-id="6a9f2-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a9f2-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a9f2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9f2-122">CommonParameters</span></span>
<span data-ttu-id="6a9f2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9f2-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9f2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9f2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a9f2-125">INPUTS</span></span>

### <span data-ttu-id="6a9f2-126">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6a9f2-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="6a9f2-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a9f2-127">OUTPUTS</span></span>

### <span data-ttu-id="6a9f2-128">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6a9f2-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="6a9f2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a9f2-129">NOTES</span></span>

## <span data-ttu-id="6a9f2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a9f2-130">RELATED LINKS</span></span>

[<span data-ttu-id="6a9f2-131">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6a9f2-131">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="6a9f2-132">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6a9f2-132">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="6a9f2-133">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6a9f2-133">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)