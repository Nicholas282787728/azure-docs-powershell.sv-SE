---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581328"
---
# <span data-ttu-id="72371-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="72371-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="72371-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72371-102">SYNOPSIS</span></span>
<span data-ttu-id="72371-103">Får en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="72371-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72371-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72371-104">SYNTAX</span></span>

### <span data-ttu-id="72371-105">ListAvailable (standard)</span><span class="sxs-lookup"><span data-stu-id="72371-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72371-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="72371-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72371-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72371-107">DESCRIPTION</span></span>
<span data-ttu-id="72371-108">Cmdleten **Get-AzureRmResourceProvider** får en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="72371-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="72371-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72371-109">EXAMPLES</span></span>

## <span data-ttu-id="72371-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72371-110">PARAMETERS</span></span>

### <span data-ttu-id="72371-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="72371-111">-ApiVersion</span></span>
<span data-ttu-id="72371-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="72371-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="72371-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="72371-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="72371-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="72371-114">-ListAvailable</span></span>
<span data-ttu-id="72371-115">Indikerar att den här åtgärden får alla tillgängliga resurs leverantörer.</span><span class="sxs-lookup"><span data-stu-id="72371-115">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="72371-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="72371-116">-Location</span></span>
<span data-ttu-id="72371-117">Anger resurs leverantörens plats.</span><span class="sxs-lookup"><span data-stu-id="72371-117">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="72371-118">-För</span><span class="sxs-lookup"><span data-stu-id="72371-118">-Pre</span></span>
<span data-ttu-id="72371-119">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="72371-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="72371-120">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="72371-120">-ProviderNamespace</span></span>
<span data-ttu-id="72371-121">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="72371-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72371-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72371-122">-DefaultProfile</span></span>
<span data-ttu-id="72371-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72371-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72371-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72371-124">CommonParameters</span></span>
<span data-ttu-id="72371-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72371-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72371-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72371-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72371-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72371-127">INPUTS</span></span>

## <span data-ttu-id="72371-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72371-128">OUTPUTS</span></span>

### <span data-ttu-id="72371-129">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="72371-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="72371-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72371-130">NOTES</span></span>

## <span data-ttu-id="72371-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72371-131">RELATED LINKS</span></span>

[<span data-ttu-id="72371-132">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="72371-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="72371-133">Avregistrera-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="72371-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


