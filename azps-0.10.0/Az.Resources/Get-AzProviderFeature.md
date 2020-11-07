---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 1296e1e135acce9d4840e625d96931f6ecc11625
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924013"
---
# <span data-ttu-id="db358-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="db358-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="db358-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db358-102">SYNOPSIS</span></span>
<span data-ttu-id="db358-103">Hämtar information om funktioner i Azure-leverantörer.</span><span class="sxs-lookup"><span data-stu-id="db358-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="db358-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db358-104">SYNTAX</span></span>

### <span data-ttu-id="db358-105">ListAvailableParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="db358-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db358-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="db358-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db358-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db358-107">DESCRIPTION</span></span>
<span data-ttu-id="db358-108">Cmdleten **Get-AzProviderFeature** får namnet, leverantörs namnet och registrerings statusen för Azure Provider-funktioner.</span><span class="sxs-lookup"><span data-stu-id="db358-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="db358-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db358-109">EXAMPLES</span></span>

### <span data-ttu-id="db358-110">Exempel 1: få alla tillgängliga funktioner</span><span class="sxs-lookup"><span data-stu-id="db358-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="db358-111">Det här kommandot får alla tillgängliga funktioner.</span><span class="sxs-lookup"><span data-stu-id="db358-111">This command gets all available features.</span></span>

### <span data-ttu-id="db358-112">Exempel 2: Hämta information om en viss funktion</span><span class="sxs-lookup"><span data-stu-id="db358-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="db358-113">Med det här kommandot får du information om funktionen AllowPreReleaseRegions för den angivna leverantören.</span><span class="sxs-lookup"><span data-stu-id="db358-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="db358-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db358-114">PARAMETERS</span></span>

### <span data-ttu-id="db358-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db358-115">-DefaultProfile</span></span>
<span data-ttu-id="db358-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="db358-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db358-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="db358-117">-FeatureName</span></span>
<span data-ttu-id="db358-118">Anger namnet på den funktion som ska visas.</span><span class="sxs-lookup"><span data-stu-id="db358-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="db358-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="db358-119">-ListAvailable</span></span>
<span data-ttu-id="db358-120">Anger att denna cmdlet får alla funktioner.</span><span class="sxs-lookup"><span data-stu-id="db358-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="db358-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="db358-121">-ProviderNamespace</span></span>
<span data-ttu-id="db358-122">Anger namn området för vilken denna cmdlet hämtar leverantörens funktioner.</span><span class="sxs-lookup"><span data-stu-id="db358-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="db358-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db358-123">CommonParameters</span></span>
<span data-ttu-id="db358-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db358-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db358-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db358-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db358-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db358-126">INPUTS</span></span>

## <span data-ttu-id="db358-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db358-127">OUTPUTS</span></span>

## <span data-ttu-id="db358-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db358-128">NOTES</span></span>

## <span data-ttu-id="db358-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db358-129">RELATED LINKS</span></span>

[<span data-ttu-id="db358-130">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="db358-130">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


