---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ca4f9431a7b382166b99a33be5b9373871b610e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928958"
---
# <span data-ttu-id="348fe-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="348fe-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="348fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="348fe-102">SYNOPSIS</span></span>
<span data-ttu-id="348fe-103">Får en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="348fe-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="348fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="348fe-104">SYNTAX</span></span>

### <span data-ttu-id="348fe-105">ListAvailable (standard)</span><span class="sxs-lookup"><span data-stu-id="348fe-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="348fe-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="348fe-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="348fe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="348fe-107">DESCRIPTION</span></span>
<span data-ttu-id="348fe-108">Cmdleten **Get-AzureRmResourceProvider** får en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="348fe-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="348fe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="348fe-109">EXAMPLES</span></span>

## <span data-ttu-id="348fe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="348fe-110">PARAMETERS</span></span>

### <span data-ttu-id="348fe-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="348fe-111">-ApiVersion</span></span>
<span data-ttu-id="348fe-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="348fe-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="348fe-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="348fe-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="348fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348fe-114">-DefaultProfile</span></span>
<span data-ttu-id="348fe-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="348fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="348fe-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="348fe-116">-ListAvailable</span></span>
<span data-ttu-id="348fe-117">Indikerar att den här åtgärden får alla tillgängliga resurs leverantörer.</span><span class="sxs-lookup"><span data-stu-id="348fe-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348fe-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="348fe-118">-Location</span></span>
<span data-ttu-id="348fe-119">Anger resurs leverantörens plats.</span><span class="sxs-lookup"><span data-stu-id="348fe-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="348fe-120">-För</span><span class="sxs-lookup"><span data-stu-id="348fe-120">-Pre</span></span>
<span data-ttu-id="348fe-121">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="348fe-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="348fe-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="348fe-122">-ProviderNamespace</span></span>
<span data-ttu-id="348fe-123">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="348fe-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348fe-124">CommonParameters</span></span>
<span data-ttu-id="348fe-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="348fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348fe-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="348fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348fe-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="348fe-127">INPUTS</span></span>

## <span data-ttu-id="348fe-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="348fe-128">OUTPUTS</span></span>

## <span data-ttu-id="348fe-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="348fe-129">NOTES</span></span>

## <span data-ttu-id="348fe-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="348fe-130">RELATED LINKS</span></span>

[<span data-ttu-id="348fe-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="348fe-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="348fe-132">Avregistrera-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="348fe-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


