---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 2371ea9a50af1d23144560acbf4fd88679f0e50d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930822"
---
# <span data-ttu-id="028bf-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="028bf-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="028bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="028bf-102">SYNOPSIS</span></span>
<span data-ttu-id="028bf-103">Registrerar en Azure-leverantör i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="028bf-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="028bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="028bf-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="028bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="028bf-105">DESCRIPTION</span></span>
<span data-ttu-id="028bf-106">**Register-AzureRmProviderFeature** cmdlet registrerar en Azure Provider-funktion på ditt konto.</span><span class="sxs-lookup"><span data-stu-id="028bf-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="028bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="028bf-107">EXAMPLES</span></span>

### <span data-ttu-id="028bf-108">Exempel 1: registrera en funktion</span><span class="sxs-lookup"><span data-stu-id="028bf-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="028bf-109">Då läggs AllowApplicationSecurityGroups-funktionen till i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="028bf-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="028bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="028bf-110">PARAMETERS</span></span>

### <span data-ttu-id="028bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028bf-111">-DefaultProfile</span></span>
<span data-ttu-id="028bf-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="028bf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="028bf-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="028bf-113">-FeatureName</span></span>
<span data-ttu-id="028bf-114">Anger namnet på den funktion som den här cmdleten registrerar.</span><span class="sxs-lookup"><span data-stu-id="028bf-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028bf-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="028bf-115">-ProviderNamespace</span></span>
<span data-ttu-id="028bf-116">Anger ett namn område som denna cmdlet registrerar en leverantörs funktion för.</span><span class="sxs-lookup"><span data-stu-id="028bf-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028bf-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="028bf-117">-Confirm</span></span>
<span data-ttu-id="028bf-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="028bf-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028bf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="028bf-119">-WhatIf</span></span>
<span data-ttu-id="028bf-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="028bf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="028bf-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="028bf-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028bf-122">CommonParameters</span></span>
<span data-ttu-id="028bf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028bf-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="028bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028bf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="028bf-125">INPUTS</span></span>

## <span data-ttu-id="028bf-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="028bf-126">OUTPUTS</span></span>

## <span data-ttu-id="028bf-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="028bf-127">NOTES</span></span>

## <span data-ttu-id="028bf-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="028bf-128">RELATED LINKS</span></span>

[<span data-ttu-id="028bf-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="028bf-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


