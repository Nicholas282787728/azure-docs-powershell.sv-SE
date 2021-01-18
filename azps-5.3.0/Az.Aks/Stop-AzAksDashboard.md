---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523312"
---
# <span data-ttu-id="4b548-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="4b548-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="4b548-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b548-102">SYNOPSIS</span></span>
<span data-ttu-id="4b548-103">Stoppa den Kubectl SSH-tunnel som skapades i Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="4b548-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="4b548-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b548-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b548-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b548-105">DESCRIPTION</span></span>
<span data-ttu-id="4b548-106">Stoppa den Kubectl SSH-tunnel som skapades i Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="4b548-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="4b548-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b548-107">EXAMPLES</span></span>

### <span data-ttu-id="4b548-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4b548-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="4b548-109">Stoppar befintlig SSH-tunnel med start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="4b548-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="4b548-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b548-110">PARAMETERS</span></span>

### <span data-ttu-id="4b548-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b548-111">-DefaultProfile</span></span>
<span data-ttu-id="4b548-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b548-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b548-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b548-113">-PassThru</span></span>
<span data-ttu-id="4b548-114">Returnerar sant om SSH-tunneln stängs.</span><span class="sxs-lookup"><span data-stu-id="4b548-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="4b548-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b548-115">CommonParameters</span></span>
<span data-ttu-id="4b548-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b548-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b548-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b548-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b548-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b548-118">INPUTS</span></span>

### <span data-ttu-id="4b548-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="4b548-119">None</span></span>

## <span data-ttu-id="4b548-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b548-120">OUTPUTS</span></span>

### <span data-ttu-id="4b548-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b548-121">System.Boolean</span></span>

## <span data-ttu-id="4b548-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b548-122">NOTES</span></span>

## <span data-ttu-id="4b548-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b548-123">RELATED LINKS</span></span>
