---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 691378cac3ac721084315a1708bf8d4d0a24dc92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575109"
---
# <span data-ttu-id="bbdef-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="bbdef-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="bbdef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbdef-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdef-103">Registrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="bbdef-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbdef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbdef-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbdef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbdef-105">DESCRIPTION</span></span>
<span data-ttu-id="bbdef-106">**Register-AzureRmResourceProvider** cmdlet registrerar en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="bbdef-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="bbdef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbdef-107">EXAMPLES</span></span>

### <span data-ttu-id="bbdef-108">Exempel 1: registrera en leverantör</span><span class="sxs-lookup"><span data-stu-id="bbdef-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="bbdef-109">Detta registrerar Microsoft. Network-leverantören för ditt konto.</span><span class="sxs-lookup"><span data-stu-id="bbdef-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="bbdef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbdef-110">PARAMETERS</span></span>

### <span data-ttu-id="bbdef-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bbdef-111">-ApiVersion</span></span>
<span data-ttu-id="bbdef-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="bbdef-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="bbdef-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="bbdef-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="bbdef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdef-114">-DefaultProfile</span></span>
<span data-ttu-id="bbdef-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bbdef-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbdef-116">-För</span><span class="sxs-lookup"><span data-stu-id="bbdef-116">-Pre</span></span>
<span data-ttu-id="bbdef-117">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="bbdef-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bbdef-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="bbdef-118">-ProviderNamespace</span></span>
<span data-ttu-id="bbdef-119">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="bbdef-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="bbdef-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bbdef-120">-Confirm</span></span>
<span data-ttu-id="bbdef-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bbdef-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdef-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdef-122">-WhatIf</span></span>
<span data-ttu-id="bbdef-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bbdef-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbdef-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bbdef-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdef-125">CommonParameters</span></span>
<span data-ttu-id="bbdef-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbdef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdef-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbdef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdef-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbdef-128">INPUTS</span></span>

## <span data-ttu-id="bbdef-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbdef-129">OUTPUTS</span></span>

## <span data-ttu-id="bbdef-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbdef-130">NOTES</span></span>

## <span data-ttu-id="bbdef-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbdef-131">RELATED LINKS</span></span>

[<span data-ttu-id="bbdef-132">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="bbdef-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="bbdef-133">Avregistrera-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="bbdef-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


