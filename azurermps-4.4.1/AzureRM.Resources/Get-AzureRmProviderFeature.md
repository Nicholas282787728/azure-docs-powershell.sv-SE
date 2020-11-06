---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581355"
---
# <span data-ttu-id="7a576-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7a576-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="7a576-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a576-102">SYNOPSIS</span></span>
<span data-ttu-id="7a576-103">Hämtar information om funktioner i Azure-leverantörer.</span><span class="sxs-lookup"><span data-stu-id="7a576-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a576-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a576-104">SYNTAX</span></span>

### <span data-ttu-id="7a576-105">ListAvailableParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7a576-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a576-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="7a576-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a576-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a576-107">DESCRIPTION</span></span>
<span data-ttu-id="7a576-108">Cmdleten **Get-AzureRmProviderFeature** får namnet, leverantörs namnet och registrerings statusen för Azure Provider-funktioner.</span><span class="sxs-lookup"><span data-stu-id="7a576-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="7a576-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a576-109">EXAMPLES</span></span>

### <span data-ttu-id="7a576-110">Exempel 1: få alla tillgängliga funktioner</span><span class="sxs-lookup"><span data-stu-id="7a576-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="7a576-111">Det här kommandot får alla tillgängliga funktioner.</span><span class="sxs-lookup"><span data-stu-id="7a576-111">This command gets all available features.</span></span>

### <span data-ttu-id="7a576-112">Exempel 2: Hämta information om en viss funktion</span><span class="sxs-lookup"><span data-stu-id="7a576-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="7a576-113">Med det här kommandot får du information om funktionen AllowPreReleaseRegions för den angivna leverantören.</span><span class="sxs-lookup"><span data-stu-id="7a576-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="7a576-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a576-114">PARAMETERS</span></span>

### <span data-ttu-id="7a576-115">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="7a576-115">-FeatureName</span></span>
<span data-ttu-id="7a576-116">Anger namnet på den funktion som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7a576-116">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a576-117">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="7a576-117">-ListAvailable</span></span>
<span data-ttu-id="7a576-118">Anger att denna cmdlet får alla funktioner.</span><span class="sxs-lookup"><span data-stu-id="7a576-118">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a576-119">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7a576-119">-ProviderNamespace</span></span>
<span data-ttu-id="7a576-120">Anger namn området för vilken denna cmdlet hämtar leverantörens funktioner.</span><span class="sxs-lookup"><span data-stu-id="7a576-120">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a576-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a576-121">-DefaultProfile</span></span>
<span data-ttu-id="7a576-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a576-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a576-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a576-123">CommonParameters</span></span>
<span data-ttu-id="7a576-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a576-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a576-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a576-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a576-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a576-126">INPUTS</span></span>

## <span data-ttu-id="7a576-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a576-127">OUTPUTS</span></span>

### <span data-ttu-id="7a576-128">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="7a576-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="7a576-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a576-129">NOTES</span></span>

## <span data-ttu-id="7a576-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a576-130">RELATED LINKS</span></span>

[<span data-ttu-id="7a576-131">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7a576-131">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


