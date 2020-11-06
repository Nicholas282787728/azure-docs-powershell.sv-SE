---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581312"
---
# <span data-ttu-id="3dd21-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="3dd21-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="3dd21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dd21-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd21-103">Registrerar en Azure-leverantör i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="3dd21-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dd21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dd21-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd21-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dd21-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd21-106">**Register-AzureRmProviderFeature** cmdlet registrerar en Azure Provider-funktion på ditt konto.</span><span class="sxs-lookup"><span data-stu-id="3dd21-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="3dd21-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dd21-107">EXAMPLES</span></span>

## <span data-ttu-id="3dd21-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dd21-108">PARAMETERS</span></span>

### <span data-ttu-id="3dd21-109">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="3dd21-109">-FeatureName</span></span>
<span data-ttu-id="3dd21-110">Anger namnet på den funktion som den här cmdleten registrerar.</span><span class="sxs-lookup"><span data-stu-id="3dd21-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="3dd21-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3dd21-111">-ProviderNamespace</span></span>
<span data-ttu-id="3dd21-112">Anger ett namn område som denna cmdlet registrerar en leverantörs funktion för.</span><span class="sxs-lookup"><span data-stu-id="3dd21-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="3dd21-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3dd21-113">-Confirm</span></span>
<span data-ttu-id="3dd21-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3dd21-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd21-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd21-115">-WhatIf</span></span>
<span data-ttu-id="3dd21-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3dd21-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd21-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3dd21-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd21-118">-DefaultProfile</span></span>
<span data-ttu-id="3dd21-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd21-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dd21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd21-120">CommonParameters</span></span>
<span data-ttu-id="3dd21-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd21-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd21-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd21-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dd21-123">INPUTS</span></span>

## <span data-ttu-id="3dd21-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dd21-124">OUTPUTS</span></span>

### <span data-ttu-id="3dd21-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="3dd21-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="3dd21-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dd21-126">NOTES</span></span>

## <span data-ttu-id="3dd21-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dd21-127">RELATED LINKS</span></span>

[<span data-ttu-id="3dd21-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="3dd21-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


