---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 182accdabc368e72451a0c1d9a1d78f1cf561730
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930090"
---
# <span data-ttu-id="3e2a5-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="3e2a5-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="3e2a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2a5-103">Hämtar information om funktioner i Azure-leverantörer.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e2a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e2a5-104">SYNTAX</span></span>

### <span data-ttu-id="3e2a5-105">ListAvailableParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3e2a5-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e2a5-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="3e2a5-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e2a5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e2a5-107">DESCRIPTION</span></span>
<span data-ttu-id="3e2a5-108">Cmdleten **Get-AzureRmProviderFeature** får namnet, leverantörs namnet och registrerings statusen för Azure Provider-funktioner.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="3e2a5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e2a5-109">EXAMPLES</span></span>

### <span data-ttu-id="3e2a5-110">Exempel 1: få alla tillgängliga funktioner</span><span class="sxs-lookup"><span data-stu-id="3e2a5-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="3e2a5-111">Det här kommandot får alla tillgängliga funktioner.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-111">This command gets all available features.</span></span>

### <span data-ttu-id="3e2a5-112">Exempel 2: Hämta information om en viss funktion</span><span class="sxs-lookup"><span data-stu-id="3e2a5-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="3e2a5-113">Med det här kommandot får du information om funktionen AllowPreReleaseRegions för den angivna leverantören.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="3e2a5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e2a5-114">PARAMETERS</span></span>

### <span data-ttu-id="3e2a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2a5-115">-DefaultProfile</span></span>
<span data-ttu-id="3e2a5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3e2a5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e2a5-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="3e2a5-117">-FeatureName</span></span>
<span data-ttu-id="3e2a5-118">Anger namnet på den funktion som ska visas.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="3e2a5-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="3e2a5-119">-ListAvailable</span></span>
<span data-ttu-id="3e2a5-120">Anger att denna cmdlet får alla funktioner.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="3e2a5-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3e2a5-121">-ProviderNamespace</span></span>
<span data-ttu-id="3e2a5-122">Anger namn området för vilken denna cmdlet hämtar leverantörens funktioner.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="3e2a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2a5-123">CommonParameters</span></span>
<span data-ttu-id="3e2a5-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2a5-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e2a5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2a5-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e2a5-126">INPUTS</span></span>

## <span data-ttu-id="3e2a5-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e2a5-127">OUTPUTS</span></span>

## <span data-ttu-id="3e2a5-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e2a5-128">NOTES</span></span>

## <span data-ttu-id="3e2a5-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e2a5-129">RELATED LINKS</span></span>

[<span data-ttu-id="3e2a5-130">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="3e2a5-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


