---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271431"
---
# <span data-ttu-id="f1734-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f1734-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="f1734-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1734-102">SYNOPSIS</span></span>
<span data-ttu-id="f1734-103">Avregistrerar en Azure-leverantör i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="f1734-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="f1734-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1734-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1734-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1734-105">DESCRIPTION</span></span>
<span data-ttu-id="f1734-106">Med cmdleten **Unregistered-AzProviderFeature** avregistrerar du en Azure Provider-funktion på ditt konto.</span><span class="sxs-lookup"><span data-stu-id="f1734-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="f1734-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1734-107">EXAMPLES</span></span>

### <span data-ttu-id="f1734-108">Exempel 1: avregistrera en funktion</span><span class="sxs-lookup"><span data-stu-id="f1734-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="f1734-109">Då avregistreras AllowApplicationSecurityGroups-funktionen för Microsoft. Network från ditt konto.</span><span class="sxs-lookup"><span data-stu-id="f1734-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="f1734-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1734-110">PARAMETERS</span></span>

### <span data-ttu-id="f1734-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1734-111">-DefaultProfile</span></span>
<span data-ttu-id="f1734-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1734-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1734-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="f1734-113">-FeatureName</span></span>
<span data-ttu-id="f1734-114">Funktionens namn.</span><span class="sxs-lookup"><span data-stu-id="f1734-114">The feature name.</span></span>

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

### <span data-ttu-id="f1734-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f1734-115">-ProviderNamespace</span></span>
<span data-ttu-id="f1734-116">Namn område för resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="f1734-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="f1734-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f1734-117">-Confirm</span></span>
<span data-ttu-id="f1734-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1734-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1734-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1734-119">-WhatIf</span></span>
<span data-ttu-id="f1734-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f1734-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1734-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f1734-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1734-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1734-122">CommonParameters</span></span>
<span data-ttu-id="f1734-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1734-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1734-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1734-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1734-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1734-125">INPUTS</span></span>

### <span data-ttu-id="f1734-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f1734-126">System.String</span></span>

## <span data-ttu-id="f1734-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1734-127">OUTPUTS</span></span>

### <span data-ttu-id="f1734-128">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f1734-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="f1734-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1734-129">NOTES</span></span>

## <span data-ttu-id="f1734-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1734-130">RELATED LINKS</span></span>