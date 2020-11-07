---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: d13eb98b01380fcb02392d1ac3f34c8d70c7f6dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756780"
---
# <span data-ttu-id="5cbf2-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5cbf2-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="5cbf2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cbf2-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbf2-103">Hämtar information om funktioner i Azure-leverantörer.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cbf2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cbf2-104">SYNTAX</span></span>

### <span data-ttu-id="5cbf2-105">ListAvailableParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5cbf2-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cbf2-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="5cbf2-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cbf2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cbf2-107">DESCRIPTION</span></span>
<span data-ttu-id="5cbf2-108">Cmdleten **Get-AzureRmProviderFeature** får namnet, leverantörs namnet och registrerings statusen för Azure Provider-funktioner.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="5cbf2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cbf2-109">EXAMPLES</span></span>

### <span data-ttu-id="5cbf2-110">Exempel 1: få alla tillgängliga funktioner</span><span class="sxs-lookup"><span data-stu-id="5cbf2-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="5cbf2-111">Det här kommandot får alla tillgängliga funktioner.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-111">This command gets all available features.</span></span>

### <span data-ttu-id="5cbf2-112">Exempel 2: Hämta information om en viss funktion</span><span class="sxs-lookup"><span data-stu-id="5cbf2-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="5cbf2-113">Med det här kommandot får du information om funktionen AllowPreReleaseRegions för den angivna leverantören.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="5cbf2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cbf2-114">PARAMETERS</span></span>

### <span data-ttu-id="5cbf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbf2-115">-DefaultProfile</span></span>
<span data-ttu-id="5cbf2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5cbf2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cbf2-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="5cbf2-117">-FeatureName</span></span>
<span data-ttu-id="5cbf2-118">Anger namnet på den funktion som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbf2-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="5cbf2-119">-ListAvailable</span></span>
<span data-ttu-id="5cbf2-120">Anger att denna cmdlet får alla funktioner.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbf2-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5cbf2-121">-ProviderNamespace</span></span>
<span data-ttu-id="5cbf2-122">Anger namn området för vilken denna cmdlet hämtar leverantörens funktioner.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbf2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbf2-123">CommonParameters</span></span>
<span data-ttu-id="5cbf2-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbf2-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbf2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbf2-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cbf2-126">INPUTS</span></span>

### <span data-ttu-id="5cbf2-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="5cbf2-127">None</span></span>
<span data-ttu-id="5cbf2-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5cbf2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cbf2-129">OUTPUTS</span></span>

### <span data-ttu-id="5cbf2-130">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="5cbf2-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="5cbf2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cbf2-131">NOTES</span></span>

## <span data-ttu-id="5cbf2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cbf2-132">RELATED LINKS</span></span>

[<span data-ttu-id="5cbf2-133">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5cbf2-133">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


