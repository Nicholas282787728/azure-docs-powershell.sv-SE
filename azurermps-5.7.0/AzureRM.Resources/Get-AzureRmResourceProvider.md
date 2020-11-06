---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: 54ce1d9fa73b29318597f5a1442712aabf7f92b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573307"
---
# <span data-ttu-id="412ff-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="412ff-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="412ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="412ff-102">SYNOPSIS</span></span>
<span data-ttu-id="412ff-103">Får en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="412ff-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="412ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="412ff-104">SYNTAX</span></span>

### <span data-ttu-id="412ff-105">ListAvailable (standard)</span><span class="sxs-lookup"><span data-stu-id="412ff-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="412ff-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="412ff-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="412ff-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="412ff-107">DESCRIPTION</span></span>
<span data-ttu-id="412ff-108">Cmdleten **Get-AzureRmResourceProvider** får en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="412ff-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="412ff-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="412ff-109">EXAMPLES</span></span>

## <span data-ttu-id="412ff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="412ff-110">PARAMETERS</span></span>

### <span data-ttu-id="412ff-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="412ff-111">-ApiVersion</span></span>
<span data-ttu-id="412ff-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="412ff-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="412ff-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="412ff-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412ff-114">-DefaultProfile</span></span>
<span data-ttu-id="412ff-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="412ff-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="412ff-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="412ff-116">-ListAvailable</span></span>
<span data-ttu-id="412ff-117">Indikerar att den här åtgärden får alla tillgängliga resurs leverantörer.</span><span class="sxs-lookup"><span data-stu-id="412ff-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ff-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="412ff-118">-Location</span></span>
<span data-ttu-id="412ff-119">Anger resurs leverantörens plats.</span><span class="sxs-lookup"><span data-stu-id="412ff-119">Specifies the location of the resource provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ff-120">-För</span><span class="sxs-lookup"><span data-stu-id="412ff-120">-Pre</span></span>
<span data-ttu-id="412ff-121">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="412ff-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="412ff-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="412ff-122">-ProviderNamespace</span></span>
<span data-ttu-id="412ff-123">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="412ff-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: String
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="412ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412ff-124">CommonParameters</span></span>
<span data-ttu-id="412ff-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="412ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412ff-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="412ff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412ff-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="412ff-127">INPUTS</span></span>

### <span data-ttu-id="412ff-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="412ff-128">None</span></span>
<span data-ttu-id="412ff-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="412ff-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="412ff-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="412ff-130">OUTPUTS</span></span>

### <span data-ttu-id="412ff-131">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="412ff-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="412ff-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="412ff-132">NOTES</span></span>

## <span data-ttu-id="412ff-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="412ff-133">RELATED LINKS</span></span>

[<span data-ttu-id="412ff-134">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="412ff-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="412ff-135">Avregistrera-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="412ff-135">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


