---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: 875dd42cb0aefd6d6422d99463cd56ace720411a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756450"
---
# <span data-ttu-id="06646-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="06646-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="06646-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06646-102">SYNOPSIS</span></span>
<span data-ttu-id="06646-103">Avregistrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="06646-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06646-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06646-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06646-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06646-105">DESCRIPTION</span></span>
<span data-ttu-id="06646-106">Med cmdleten **Unregistered-AzureRmResourceProvider** avregistrerar du en Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="06646-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="06646-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06646-107">EXAMPLES</span></span>

## <span data-ttu-id="06646-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06646-108">PARAMETERS</span></span>

### <span data-ttu-id="06646-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06646-109">-ApiVersion</span></span>
<span data-ttu-id="06646-110">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="06646-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="06646-111">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="06646-111">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06646-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06646-112">-DefaultProfile</span></span>
<span data-ttu-id="06646-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="06646-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06646-114">-För</span><span class="sxs-lookup"><span data-stu-id="06646-114">-Pre</span></span>
<span data-ttu-id="06646-115">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="06646-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06646-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="06646-116">-ProviderNamespace</span></span>
<span data-ttu-id="06646-117">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="06646-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="06646-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06646-118">-Confirm</span></span>
<span data-ttu-id="06646-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06646-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06646-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06646-120">-WhatIf</span></span>
<span data-ttu-id="06646-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06646-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06646-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06646-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06646-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06646-123">CommonParameters</span></span>
<span data-ttu-id="06646-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06646-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06646-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06646-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06646-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06646-126">INPUTS</span></span>

### <span data-ttu-id="06646-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="06646-127">None</span></span>
<span data-ttu-id="06646-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="06646-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06646-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06646-129">OUTPUTS</span></span>

### <span data-ttu-id="06646-130">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider]</span><span class="sxs-lookup"><span data-stu-id="06646-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider]</span></span>

## <span data-ttu-id="06646-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06646-131">NOTES</span></span>

## <span data-ttu-id="06646-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06646-132">RELATED LINKS</span></span>

[<span data-ttu-id="06646-133">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="06646-133">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="06646-134">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="06646-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


