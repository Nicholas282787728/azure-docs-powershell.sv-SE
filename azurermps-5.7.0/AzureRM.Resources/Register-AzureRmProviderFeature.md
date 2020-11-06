---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b41f7cb1c5e3ebec58e3866c94d8e2c62bdf670b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575519"
---
# <span data-ttu-id="53be6-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="53be6-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="53be6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53be6-102">SYNOPSIS</span></span>
<span data-ttu-id="53be6-103">Registrerar en Azure-leverantör i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="53be6-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53be6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53be6-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53be6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53be6-105">DESCRIPTION</span></span>
<span data-ttu-id="53be6-106">**Register-AzureRmProviderFeature** cmdlet registrerar en Azure Provider-funktion på ditt konto.</span><span class="sxs-lookup"><span data-stu-id="53be6-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="53be6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53be6-107">EXAMPLES</span></span>

### <span data-ttu-id="53be6-108">Exempel 1: registrera en funktion</span><span class="sxs-lookup"><span data-stu-id="53be6-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="53be6-109">Då läggs AllowApplicationSecurityGroups-funktionen till i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="53be6-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="53be6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53be6-110">PARAMETERS</span></span>

### <span data-ttu-id="53be6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53be6-111">-DefaultProfile</span></span>
<span data-ttu-id="53be6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="53be6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53be6-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="53be6-113">-FeatureName</span></span>
<span data-ttu-id="53be6-114">Anger namnet på den funktion som den här cmdleten registrerar.</span><span class="sxs-lookup"><span data-stu-id="53be6-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="53be6-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="53be6-115">-ProviderNamespace</span></span>
<span data-ttu-id="53be6-116">Anger ett namn område som denna cmdlet registrerar en leverantörs funktion för.</span><span class="sxs-lookup"><span data-stu-id="53be6-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="53be6-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53be6-117">-Confirm</span></span>
<span data-ttu-id="53be6-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53be6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53be6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53be6-119">-WhatIf</span></span>
<span data-ttu-id="53be6-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53be6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53be6-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53be6-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53be6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53be6-122">CommonParameters</span></span>
<span data-ttu-id="53be6-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53be6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53be6-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53be6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53be6-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53be6-125">INPUTS</span></span>

### <span data-ttu-id="53be6-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="53be6-126">None</span></span>
<span data-ttu-id="53be6-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="53be6-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53be6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53be6-128">OUTPUTS</span></span>

### <span data-ttu-id="53be6-129">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="53be6-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="53be6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53be6-130">NOTES</span></span>

## <span data-ttu-id="53be6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53be6-131">RELATED LINKS</span></span>

[<span data-ttu-id="53be6-132">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="53be6-132">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


