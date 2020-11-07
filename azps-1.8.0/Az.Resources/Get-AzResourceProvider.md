---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 76a0164a5cf4c4d67ecb7f64667b9b87d9bc252c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747139"
---
# <span data-ttu-id="34b49-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="34b49-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="34b49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34b49-102">SYNOPSIS</span></span>
<span data-ttu-id="34b49-103">Får en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="34b49-103">Gets a resource provider.</span></span>

## <span data-ttu-id="34b49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34b49-104">SYNTAX</span></span>

### <span data-ttu-id="34b49-105">ListAvailable (standard)</span><span class="sxs-lookup"><span data-stu-id="34b49-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34b49-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="34b49-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34b49-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34b49-107">DESCRIPTION</span></span>
<span data-ttu-id="34b49-108">Cmdleten **Get-AzResourceProvider** får en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="34b49-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="34b49-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34b49-109">EXAMPLES</span></span>

## <span data-ttu-id="34b49-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34b49-110">PARAMETERS</span></span>

### <span data-ttu-id="34b49-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34b49-111">-ApiVersion</span></span>
<span data-ttu-id="34b49-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="34b49-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="34b49-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="34b49-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="34b49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b49-114">-DefaultProfile</span></span>
<span data-ttu-id="34b49-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="34b49-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34b49-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="34b49-116">-ListAvailable</span></span>
<span data-ttu-id="34b49-117">Indikerar att den här åtgärden får alla tillgängliga resurs leverantörer.</span><span class="sxs-lookup"><span data-stu-id="34b49-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="34b49-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="34b49-118">-Location</span></span>
<span data-ttu-id="34b49-119">Anger resurs leverantörens plats.</span><span class="sxs-lookup"><span data-stu-id="34b49-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="34b49-120">-För</span><span class="sxs-lookup"><span data-stu-id="34b49-120">-Pre</span></span>
<span data-ttu-id="34b49-121">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="34b49-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="34b49-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="34b49-122">-ProviderNamespace</span></span>
<span data-ttu-id="34b49-123">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="34b49-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="34b49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b49-124">CommonParameters</span></span>
<span data-ttu-id="34b49-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b49-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b49-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b49-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34b49-127">INPUTS</span></span>

### <span data-ttu-id="34b49-128">System. string []</span><span class="sxs-lookup"><span data-stu-id="34b49-128">System.String[]</span></span>

## <span data-ttu-id="34b49-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34b49-129">OUTPUTS</span></span>

### <span data-ttu-id="34b49-130">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="34b49-130">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="34b49-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34b49-131">NOTES</span></span>

## <span data-ttu-id="34b49-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34b49-132">RELATED LINKS</span></span>

[<span data-ttu-id="34b49-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="34b49-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="34b49-134">Avregistrera-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="34b49-134">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


