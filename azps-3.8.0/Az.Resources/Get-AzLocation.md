---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090049"
---
# <span data-ttu-id="671c2-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="671c2-101">Get-AzLocation</span></span>

## <span data-ttu-id="671c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="671c2-102">SYNOPSIS</span></span>
<span data-ttu-id="671c2-103">Hämtar alla platser och leverantörs leverantörer för varje plats.</span><span class="sxs-lookup"><span data-stu-id="671c2-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="671c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="671c2-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="671c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="671c2-105">DESCRIPTION</span></span>
<span data-ttu-id="671c2-106">Cmdleten **Get-AzLocation** hämtar alla platser och de tillgängliga leverantörerna för varje plats.</span><span class="sxs-lookup"><span data-stu-id="671c2-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="671c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="671c2-107">EXAMPLES</span></span>

### <span data-ttu-id="671c2-108">Exempel 1: Hämta alla platser och de tillgängliga leverantörerna</span><span class="sxs-lookup"><span data-stu-id="671c2-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="671c2-109">Det här kommandot får alla platser och leverantörs leverantörer för varje plats.</span><span class="sxs-lookup"><span data-stu-id="671c2-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="671c2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="671c2-110">PARAMETERS</span></span>

### <span data-ttu-id="671c2-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="671c2-111">-ApiVersion</span></span>
<span data-ttu-id="671c2-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="671c2-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="671c2-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="671c2-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="671c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="671c2-114">-DefaultProfile</span></span>
<span data-ttu-id="671c2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="671c2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="671c2-116">-För</span><span class="sxs-lookup"><span data-stu-id="671c2-116">-Pre</span></span>
<span data-ttu-id="671c2-117">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="671c2-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="671c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="671c2-118">CommonParameters</span></span>
<span data-ttu-id="671c2-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="671c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="671c2-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="671c2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="671c2-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="671c2-121">INPUTS</span></span>

### <span data-ttu-id="671c2-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="671c2-122">None</span></span>

## <span data-ttu-id="671c2-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="671c2-123">OUTPUTS</span></span>

### <span data-ttu-id="671c2-124">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="671c2-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="671c2-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="671c2-125">NOTES</span></span>

## <span data-ttu-id="671c2-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="671c2-126">RELATED LINKS</span></span>
