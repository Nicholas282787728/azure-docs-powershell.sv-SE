---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 691d8cf006e720d706d2473f76ff8660927e73ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263308"
---
# <span data-ttu-id="ba4f1-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ba4f1-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="ba4f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4f1-103">Få användning av en Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="ba4f1-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ba4f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba4f1-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba4f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba4f1-105">DESCRIPTION</span></span>
<span data-ttu-id="ba4f1-106">Få användning av en Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="ba4f1-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ba4f1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba4f1-107">EXAMPLES</span></span>

### <span data-ttu-id="ba4f1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ba4f1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="ba4f1-109">Få användning av en Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="ba4f1-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ba4f1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba4f1-110">PARAMETERS</span></span>

### <span data-ttu-id="ba4f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4f1-111">-DefaultProfile</span></span>
<span data-ttu-id="ba4f1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba4f1-113">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ba4f1-113">-RegistryName</span></span>
<span data-ttu-id="ba4f1-114">Mål register namn.</span><span class="sxs-lookup"><span data-stu-id="ba4f1-114">Target registry name.</span></span>

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

### <span data-ttu-id="ba4f1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba4f1-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba4f1-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ba4f1-116">Resource group name.</span></span>

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

### <span data-ttu-id="ba4f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4f1-117">CommonParameters</span></span>
<span data-ttu-id="ba4f1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba4f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4f1-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba4f1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4f1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba4f1-120">INPUTS</span></span>

### <span data-ttu-id="ba4f1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ba4f1-121">System.String</span></span>

## <span data-ttu-id="ba4f1-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba4f1-122">OUTPUTS</span></span>

### <span data-ttu-id="ba4f1-123">Microsoft. Azure. commands. ContainerRegistry. Models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ba4f1-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="ba4f1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba4f1-124">NOTES</span></span>

## <span data-ttu-id="ba4f1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba4f1-125">RELATED LINKS</span></span>
