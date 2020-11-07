---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
ms.openlocfilehash: c5d9d2131ff144f04794d2cf283aaf51ed1450e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930114"
---
# <span data-ttu-id="36eb6-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="36eb6-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="36eb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="36eb6-103">Hämtar alla platser och leverantörs leverantörer för varje plats.</span><span class="sxs-lookup"><span data-stu-id="36eb6-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36eb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36eb6-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36eb6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="36eb6-106">Cmdleten **Get-AzureRmLocation** hämtar alla platser och de tillgängliga leverantörerna för varje plats.</span><span class="sxs-lookup"><span data-stu-id="36eb6-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="36eb6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="36eb6-108">Exempel 1: Hämta alla platser och de tillgängliga leverantörerna</span><span class="sxs-lookup"><span data-stu-id="36eb6-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="36eb6-109">Det här kommandot får alla platser och leverantörs leverantörer för varje plats.</span><span class="sxs-lookup"><span data-stu-id="36eb6-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="36eb6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36eb6-110">PARAMETERS</span></span>

### <span data-ttu-id="36eb6-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="36eb6-111">-ApiVersion</span></span>
<span data-ttu-id="36eb6-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="36eb6-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="36eb6-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="36eb6-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="36eb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36eb6-114">-DefaultProfile</span></span>
<span data-ttu-id="36eb6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="36eb6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36eb6-116">-För</span><span class="sxs-lookup"><span data-stu-id="36eb6-116">-Pre</span></span>
<span data-ttu-id="36eb6-117">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="36eb6-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="36eb6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36eb6-118">CommonParameters</span></span>
<span data-ttu-id="36eb6-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36eb6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36eb6-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36eb6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36eb6-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36eb6-121">INPUTS</span></span>

## <span data-ttu-id="36eb6-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36eb6-122">OUTPUTS</span></span>

## <span data-ttu-id="36eb6-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36eb6-123">NOTES</span></span>

## <span data-ttu-id="36eb6-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36eb6-124">RELATED LINKS</span></span>
