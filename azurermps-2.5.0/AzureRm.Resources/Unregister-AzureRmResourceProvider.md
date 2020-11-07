---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ead0edddccc5372c04e2e4b77d7860bbad29c27a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929602"
---
# <span data-ttu-id="9d20a-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9d20a-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="9d20a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d20a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d20a-103">Avregistrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="9d20a-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d20a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d20a-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d20a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d20a-105">DESCRIPTION</span></span>
<span data-ttu-id="9d20a-106">Med cmdleten **Unregistered-AzureRmResourceProvider** avregistrerar du en Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="9d20a-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="9d20a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d20a-107">EXAMPLES</span></span>

## <span data-ttu-id="9d20a-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d20a-108">PARAMETERS</span></span>

### <span data-ttu-id="9d20a-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9d20a-109">-ApiVersion</span></span>
<span data-ttu-id="9d20a-110">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="9d20a-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9d20a-111">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="9d20a-111">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d20a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d20a-112">-DefaultProfile</span></span>
<span data-ttu-id="9d20a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9d20a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d20a-114">-För</span><span class="sxs-lookup"><span data-stu-id="9d20a-114">-Pre</span></span>
<span data-ttu-id="9d20a-115">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="9d20a-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d20a-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="9d20a-116">-ProviderNamespace</span></span>
<span data-ttu-id="9d20a-117">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="9d20a-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="9d20a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9d20a-118">-Confirm</span></span>
<span data-ttu-id="9d20a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d20a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d20a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d20a-120">-WhatIf</span></span>
<span data-ttu-id="9d20a-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9d20a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d20a-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9d20a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d20a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d20a-123">CommonParameters</span></span>
<span data-ttu-id="9d20a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d20a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d20a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d20a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d20a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d20a-126">INPUTS</span></span>

## <span data-ttu-id="9d20a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d20a-127">OUTPUTS</span></span>

## <span data-ttu-id="9d20a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d20a-128">NOTES</span></span>

## <span data-ttu-id="9d20a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d20a-129">RELATED LINKS</span></span>

[<span data-ttu-id="9d20a-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9d20a-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="9d20a-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9d20a-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


