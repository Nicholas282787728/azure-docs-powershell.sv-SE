---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: c3459a07eb6f92e4ec30b5018efc41ff13e1c41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930814"
---
# <span data-ttu-id="3b584-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b584-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="3b584-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b584-102">SYNOPSIS</span></span>
<span data-ttu-id="3b584-103">Registrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="3b584-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b584-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b584-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b584-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b584-105">DESCRIPTION</span></span>
<span data-ttu-id="3b584-106">**Register-AzureRmResourceProvider** cmdlet registrerar en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="3b584-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="3b584-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b584-107">EXAMPLES</span></span>

### <span data-ttu-id="3b584-108">Exempel 1: registrera en leverantör</span><span class="sxs-lookup"><span data-stu-id="3b584-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="3b584-109">Detta registrerar Microsoft. Network-leverantören för ditt konto.</span><span class="sxs-lookup"><span data-stu-id="3b584-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="3b584-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b584-110">PARAMETERS</span></span>

### <span data-ttu-id="3b584-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3b584-111">-ApiVersion</span></span>
<span data-ttu-id="3b584-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="3b584-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3b584-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="3b584-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3b584-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b584-114">-DefaultProfile</span></span>
<span data-ttu-id="3b584-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3b584-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b584-116">-För</span><span class="sxs-lookup"><span data-stu-id="3b584-116">-Pre</span></span>
<span data-ttu-id="3b584-117">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3b584-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3b584-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3b584-118">-ProviderNamespace</span></span>
<span data-ttu-id="3b584-119">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="3b584-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="3b584-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b584-120">-Confirm</span></span>
<span data-ttu-id="3b584-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b584-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b584-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b584-122">-WhatIf</span></span>
<span data-ttu-id="3b584-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b584-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b584-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b584-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b584-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b584-125">CommonParameters</span></span>
<span data-ttu-id="3b584-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b584-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b584-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b584-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b584-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b584-128">INPUTS</span></span>

## <span data-ttu-id="3b584-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b584-129">OUTPUTS</span></span>

## <span data-ttu-id="3b584-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b584-130">NOTES</span></span>

## <span data-ttu-id="3b584-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b584-131">RELATED LINKS</span></span>

[<span data-ttu-id="3b584-132">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b584-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="3b584-133">Avregistrera-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b584-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


