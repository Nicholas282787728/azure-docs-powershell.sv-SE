---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270345"
---
# <span data-ttu-id="87bcc-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="87bcc-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="87bcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="87bcc-103">Lista tillgänglig version för att skapa hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="87bcc-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="87bcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87bcc-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87bcc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87bcc-105">DESCRIPTION</span></span>
<span data-ttu-id="87bcc-106">Lista tillgänglig version för att skapa hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="87bcc-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="87bcc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87bcc-107">EXAMPLES</span></span>

### <span data-ttu-id="87bcc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="87bcc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="87bcc-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87bcc-109">PARAMETERS</span></span>

### <span data-ttu-id="87bcc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87bcc-110">-DefaultProfile</span></span>
<span data-ttu-id="87bcc-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87bcc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87bcc-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="87bcc-112">-Location</span></span>
<span data-ttu-id="87bcc-113">Azure-plats för klustret.</span><span class="sxs-lookup"><span data-stu-id="87bcc-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="87bcc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bcc-114">CommonParameters</span></span>
<span data-ttu-id="87bcc-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87bcc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87bcc-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87bcc-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bcc-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87bcc-117">INPUTS</span></span>

### <span data-ttu-id="87bcc-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="87bcc-118">None</span></span>

## <span data-ttu-id="87bcc-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87bcc-119">OUTPUTS</span></span>

### <span data-ttu-id="87bcc-120">Microsoft. Azure. commands. AKS. Models. PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="87bcc-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="87bcc-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87bcc-121">NOTES</span></span>

## <span data-ttu-id="87bcc-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87bcc-122">RELATED LINKS</span></span>
