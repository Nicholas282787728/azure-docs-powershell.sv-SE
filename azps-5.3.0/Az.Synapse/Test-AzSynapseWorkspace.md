---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523383"
---
# <span data-ttu-id="162c3-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="162c3-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="162c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="162c3-102">SYNOPSIS</span></span>
<span data-ttu-id="162c3-103">Kontrollerar om det finns en Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="162c3-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="162c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="162c3-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="162c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="162c3-105">DESCRIPTION</span></span>
<span data-ttu-id="162c3-106">**Testet AzSynapseWorkspace-** cmdlet söker efter en Synapse-BA-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="162c3-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="162c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="162c3-107">EXAMPLES</span></span>

### <span data-ttu-id="162c3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="162c3-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="162c3-109">Det här kommandot kontrollerar om det finns en Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="162c3-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="162c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="162c3-110">PARAMETERS</span></span>

### <span data-ttu-id="162c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162c3-111">-DefaultProfile</span></span>
<span data-ttu-id="162c3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="162c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="162c3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="162c3-113">-Name</span></span>
<span data-ttu-id="162c3-114">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="162c3-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="162c3-115">-ResourceGroupName</span></span>
<span data-ttu-id="162c3-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="162c3-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162c3-117">CommonParameters</span></span>
<span data-ttu-id="162c3-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="162c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162c3-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="162c3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162c3-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="162c3-120">INPUTS</span></span>

### <span data-ttu-id="162c3-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="162c3-121">None</span></span>

## <span data-ttu-id="162c3-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="162c3-122">OUTPUTS</span></span>

### <span data-ttu-id="162c3-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="162c3-123">System.Object</span></span>
## <span data-ttu-id="162c3-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="162c3-124">NOTES</span></span>

## <span data-ttu-id="162c3-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="162c3-125">RELATED LINKS</span></span>
