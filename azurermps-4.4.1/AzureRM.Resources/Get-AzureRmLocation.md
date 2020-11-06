---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 62acee0398c9530a54e02c2347bf384498b07196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584540"
---
# <span data-ttu-id="df323-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="df323-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="df323-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df323-102">SYNOPSIS</span></span>
<span data-ttu-id="df323-103">Hämtar alla platser och leverantörs leverantörer för varje plats.</span><span class="sxs-lookup"><span data-stu-id="df323-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df323-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df323-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df323-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df323-105">DESCRIPTION</span></span>
<span data-ttu-id="df323-106">Cmdleten **Get-AzureRmLocation** hämtar alla platser och de tillgängliga leverantörerna för varje plats.</span><span class="sxs-lookup"><span data-stu-id="df323-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="df323-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df323-107">EXAMPLES</span></span>

### <span data-ttu-id="df323-108">Exempel 1: Hämta alla platser och de tillgängliga leverantörerna</span><span class="sxs-lookup"><span data-stu-id="df323-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="df323-109">Det här kommandot får alla platser och leverantörs leverantörer för varje plats.</span><span class="sxs-lookup"><span data-stu-id="df323-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="df323-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df323-110">PARAMETERS</span></span>

### <span data-ttu-id="df323-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="df323-111">-ApiVersion</span></span>
<span data-ttu-id="df323-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="df323-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="df323-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="df323-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="df323-114">-För</span><span class="sxs-lookup"><span data-stu-id="df323-114">-Pre</span></span>
<span data-ttu-id="df323-115">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="df323-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="df323-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df323-116">-DefaultProfile</span></span>
<span data-ttu-id="df323-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df323-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df323-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df323-118">CommonParameters</span></span>
<span data-ttu-id="df323-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df323-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df323-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df323-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df323-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df323-121">INPUTS</span></span>

## <span data-ttu-id="df323-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df323-122">OUTPUTS</span></span>

### <span data-ttu-id="df323-123">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProviderLocation]</span><span class="sxs-lookup"><span data-stu-id="df323-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="df323-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df323-124">NOTES</span></span>

## <span data-ttu-id="df323-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df323-125">RELATED LINKS</span></span>

