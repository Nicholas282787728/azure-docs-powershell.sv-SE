---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 6cb27f66871038fa1849671391e1d7d9f8f3ccd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258641"
---
# <span data-ttu-id="18988-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="18988-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="18988-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18988-102">SYNOPSIS</span></span>
<span data-ttu-id="18988-103">Avregistrerar en Azure-leverantör i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="18988-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="18988-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18988-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18988-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18988-105">DESCRIPTION</span></span>
<span data-ttu-id="18988-106">Med cmdleten **Unregistered-AzProviderFeature** avregistrerar du en Azure Provider-funktion på ditt konto.</span><span class="sxs-lookup"><span data-stu-id="18988-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="18988-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18988-107">EXAMPLES</span></span>

### <span data-ttu-id="18988-108">Exempel 1: avregistrera en funktion</span><span class="sxs-lookup"><span data-stu-id="18988-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="18988-109">Då avregistreras AllowApplicationSecurityGroups-funktionen för Microsoft. Network från ditt konto.</span><span class="sxs-lookup"><span data-stu-id="18988-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="18988-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18988-110">PARAMETERS</span></span>

### <span data-ttu-id="18988-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18988-111">-DefaultProfile</span></span>
<span data-ttu-id="18988-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18988-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18988-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="18988-113">-FeatureName</span></span>
<span data-ttu-id="18988-114">Funktionens namn.</span><span class="sxs-lookup"><span data-stu-id="18988-114">The feature name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18988-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="18988-115">-ProviderNamespace</span></span>
<span data-ttu-id="18988-116">Namn område för resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="18988-116">The resource provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18988-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18988-117">-Confirm</span></span>
<span data-ttu-id="18988-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18988-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18988-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18988-119">-WhatIf</span></span>
<span data-ttu-id="18988-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18988-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18988-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18988-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18988-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18988-122">CommonParameters</span></span>
<span data-ttu-id="18988-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18988-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18988-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18988-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18988-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18988-125">INPUTS</span></span>

### <span data-ttu-id="18988-126">System. String</span><span class="sxs-lookup"><span data-stu-id="18988-126">System.String</span></span>

## <span data-ttu-id="18988-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18988-127">OUTPUTS</span></span>

### <span data-ttu-id="18988-128">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="18988-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="18988-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18988-129">NOTES</span></span>

## <span data-ttu-id="18988-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18988-130">RELATED LINKS</span></span>
