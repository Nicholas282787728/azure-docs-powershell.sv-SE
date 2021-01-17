---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389022"
---
# <span data-ttu-id="0ff2a-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="0ff2a-101">Get-AzLocation</span></span>

## <span data-ttu-id="0ff2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ff2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff2a-103">Hämtar alla platser och leverantörs leverantörer för varje plats.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="0ff2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ff2a-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ff2a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ff2a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff2a-106">Cmdleten **Get-AzLocation** hämtar alla platser och de tillgängliga leverantörerna för varje plats.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="0ff2a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ff2a-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff2a-108">Exempel 1: Hämta alla platser och de tillgängliga leverantörerna</span><span class="sxs-lookup"><span data-stu-id="0ff2a-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="0ff2a-109">Det här kommandot får alla platser och leverantörs leverantörer för varje plats.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="0ff2a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ff2a-110">PARAMETERS</span></span>

### <span data-ttu-id="0ff2a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0ff2a-111">-ApiVersion</span></span>
<span data-ttu-id="0ff2a-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0ff2a-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0ff2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff2a-114">-DefaultProfile</span></span>
<span data-ttu-id="0ff2a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0ff2a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ff2a-116">-För</span><span class="sxs-lookup"><span data-stu-id="0ff2a-116">-Pre</span></span>
<span data-ttu-id="0ff2a-117">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0ff2a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff2a-118">CommonParameters</span></span>
<span data-ttu-id="0ff2a-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff2a-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ff2a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff2a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ff2a-121">INPUTS</span></span>

### <span data-ttu-id="0ff2a-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="0ff2a-122">None</span></span>

## <span data-ttu-id="0ff2a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ff2a-123">OUTPUTS</span></span>

### <span data-ttu-id="0ff2a-124">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="0ff2a-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="0ff2a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ff2a-125">NOTES</span></span>

## <span data-ttu-id="0ff2a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ff2a-126">RELATED LINKS</span></span>
