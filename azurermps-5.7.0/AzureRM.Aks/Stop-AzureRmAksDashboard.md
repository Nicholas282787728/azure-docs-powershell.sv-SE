---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 4ec1c8c2788469ffd377127bc58f657c817434a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581231"
---
# <span data-ttu-id="b6f53-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="b6f53-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="b6f53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6f53-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f53-103">Stoppa den Kubectl SSH-tunnel som skapades i Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="b6f53-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6f53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6f53-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6f53-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6f53-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f53-106">Stoppa den Kubectl SSH-tunnel som skapades i Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="b6f53-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="b6f53-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6f53-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f53-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6f53-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="b6f53-109">Stoppar befintlig SSH-tunnel med start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="b6f53-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="b6f53-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6f53-110">PARAMETERS</span></span>

### <span data-ttu-id="b6f53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f53-111">-DefaultProfile</span></span>
<span data-ttu-id="b6f53-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f53-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f53-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6f53-113">-PassThru</span></span>
<span data-ttu-id="b6f53-114">Returnerar sant om SSH-tunneln stängs.</span><span class="sxs-lookup"><span data-stu-id="b6f53-114">Returns true if SSH tunnel is closed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f53-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f53-115">CommonParameters</span></span>
<span data-ttu-id="b6f53-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f53-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f53-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f53-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f53-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6f53-118">INPUTS</span></span>

### <span data-ttu-id="b6f53-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="b6f53-119">None</span></span>

## <span data-ttu-id="b6f53-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6f53-120">OUTPUTS</span></span>

### <span data-ttu-id="b6f53-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6f53-121">System.Boolean</span></span>

## <span data-ttu-id="b6f53-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6f53-122">NOTES</span></span>

## <span data-ttu-id="b6f53-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6f53-123">RELATED LINKS</span></span>
