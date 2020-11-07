---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 46a18d981bae7a8528a866d4f21cf5b07b64732f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747154"
---
# <span data-ttu-id="6e4e5-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6e4e5-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="6e4e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4e5-103">Hämtar information om funktioner i Azure-leverantörer.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="6e4e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e4e5-104">SYNTAX</span></span>

### <span data-ttu-id="6e4e5-105">ListAvailableParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6e4e5-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e4e5-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="6e4e5-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e4e5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e4e5-107">DESCRIPTION</span></span>
<span data-ttu-id="6e4e5-108">Cmdleten **Get-AzProviderFeature** får namnet, leverantörs namnet och registrerings statusen för Azure Provider-funktioner.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="6e4e5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e4e5-109">EXAMPLES</span></span>

### <span data-ttu-id="6e4e5-110">Exempel 1: få alla tillgängliga funktioner</span><span class="sxs-lookup"><span data-stu-id="6e4e5-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="6e4e5-111">Det här kommandot får alla tillgängliga funktioner.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-111">This command gets all available features.</span></span>

### <span data-ttu-id="6e4e5-112">Exempel 2: Hämta information om en viss funktion</span><span class="sxs-lookup"><span data-stu-id="6e4e5-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="6e4e5-113">Med det här kommandot får du information om funktionen AllowPreReleaseRegions för den angivna leverantören.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="6e4e5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e4e5-114">PARAMETERS</span></span>

### <span data-ttu-id="6e4e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4e5-115">-DefaultProfile</span></span>
<span data-ttu-id="6e4e5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6e4e5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e4e5-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="6e4e5-117">-FeatureName</span></span>
<span data-ttu-id="6e4e5-118">Anger namnet på den funktion som ska visas.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="6e4e5-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="6e4e5-119">-ListAvailable</span></span>
<span data-ttu-id="6e4e5-120">Anger att denna cmdlet får alla funktioner.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="6e4e5-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="6e4e5-121">-ProviderNamespace</span></span>
<span data-ttu-id="6e4e5-122">Anger namn området för vilken denna cmdlet hämtar leverantörens funktioner.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="6e4e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4e5-123">CommonParameters</span></span>
<span data-ttu-id="6e4e5-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e4e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4e5-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e4e5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4e5-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e4e5-126">INPUTS</span></span>

### <span data-ttu-id="6e4e5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6e4e5-127">System.String</span></span>

## <span data-ttu-id="6e4e5-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e4e5-128">OUTPUTS</span></span>

### <span data-ttu-id="6e4e5-129">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6e4e5-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="6e4e5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e4e5-130">NOTES</span></span>

## <span data-ttu-id="6e4e5-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e4e5-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e4e5-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6e4e5-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)

