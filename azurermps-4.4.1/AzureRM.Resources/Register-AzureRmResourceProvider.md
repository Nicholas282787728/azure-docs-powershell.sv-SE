---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 92d94950bc4bc90494482b22b81cbd918c8b6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581303"
---
# <span data-ttu-id="3b554-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b554-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="3b554-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b554-102">SYNOPSIS</span></span>
<span data-ttu-id="3b554-103">Registrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="3b554-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b554-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b554-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b554-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b554-105">DESCRIPTION</span></span>
<span data-ttu-id="3b554-106">**Register-AzureRmResourceProvider** cmdlet registrerar en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="3b554-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="3b554-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b554-107">EXAMPLES</span></span>

## <span data-ttu-id="3b554-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b554-108">PARAMETERS</span></span>

### <span data-ttu-id="3b554-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3b554-109">-ApiVersion</span></span>
<span data-ttu-id="3b554-110">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="3b554-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3b554-111">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="3b554-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3b554-112">-För</span><span class="sxs-lookup"><span data-stu-id="3b554-112">-Pre</span></span>
<span data-ttu-id="3b554-113">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3b554-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3b554-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3b554-114">-ProviderNamespace</span></span>
<span data-ttu-id="3b554-115">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="3b554-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="3b554-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b554-116">-Confirm</span></span>
<span data-ttu-id="3b554-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b554-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b554-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b554-118">-WhatIf</span></span>
<span data-ttu-id="3b554-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b554-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b554-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b554-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b554-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b554-121">-DefaultProfile</span></span>
<span data-ttu-id="3b554-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b554-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b554-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b554-123">CommonParameters</span></span>
<span data-ttu-id="3b554-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b554-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b554-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b554-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b554-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b554-126">INPUTS</span></span>

## <span data-ttu-id="3b554-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b554-127">OUTPUTS</span></span>

### <span data-ttu-id="3b554-128">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b554-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="3b554-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b554-129">NOTES</span></span>

## <span data-ttu-id="3b554-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b554-130">RELATED LINKS</span></span>

[<span data-ttu-id="3b554-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b554-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="3b554-132">Avregistrera-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b554-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


