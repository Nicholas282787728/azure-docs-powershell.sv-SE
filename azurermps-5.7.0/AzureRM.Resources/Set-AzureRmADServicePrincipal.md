---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 853404bce6d45f2824c574b249c434ccebc281ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583040"
---
# <span data-ttu-id="4ffe3-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4ffe3-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="4ffe3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ffe3-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffe3-103">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ffe3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ffe3-104">SYNTAX</span></span>

### <span data-ttu-id="4ffe3-105">SpObjectIdWithDisplayNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4ffe3-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ffe3-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ffe3-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ffe3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ffe3-107">DESCRIPTION</span></span>
<span data-ttu-id="4ffe3-108">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="4ffe3-109">Använd New-AzureRmADSpCredential cmdlet för att uppdatera autentiseringsuppgifterna som är associerade med den här tjänstens huvud säkerhets objekt.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="4ffe3-110">Använd Set-AzureRmADApplication cmdlet för att uppdatera egenskaperna för det underliggande programmet.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="4ffe3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ffe3-111">EXAMPLES</span></span>

### <span data-ttu-id="4ffe3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ffe3-112">Example 1</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="4ffe3-113">Uppdaterar visnings namnet för tjänstens huvud konto med angivet objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="4ffe3-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4ffe3-114">Example 2</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="4ffe3-115">Uppdaterar visnings namnet för tjänstens huvud namn med angivet SPN.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="4ffe3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ffe3-116">PARAMETERS</span></span>

### <span data-ttu-id="4ffe3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffe3-117">-DefaultProfile</span></span>
<span data-ttu-id="4ffe3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4ffe3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ffe3-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4ffe3-119">-DisplayName</span></span>
<span data-ttu-id="4ffe3-120">Nytt visnings namn för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-120">New display name for the service principal.</span></span>

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

### <span data-ttu-id="4ffe3-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4ffe3-121">-ObjectId</span></span>
<span data-ttu-id="4ffe3-122">Objekt-ID för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-122">The object id of the service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ffe3-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4ffe3-123">-ServicePrincipalName</span></span>
<span data-ttu-id="4ffe3-124">SPN för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-124">The SPN of service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ffe3-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ffe3-125">-Confirm</span></span>
<span data-ttu-id="4ffe3-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ffe3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ffe3-127">-WhatIf</span></span>
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

### <span data-ttu-id="4ffe3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffe3-128">CommonParameters</span></span>
<span data-ttu-id="4ffe3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffe3-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffe3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffe3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ffe3-131">INPUTS</span></span>

### <span data-ttu-id="4ffe3-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="4ffe3-132">None</span></span>
<span data-ttu-id="4ffe3-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4ffe3-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ffe3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ffe3-134">OUTPUTS</span></span>

## <span data-ttu-id="4ffe3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ffe3-135">NOTES</span></span>

## <span data-ttu-id="4ffe3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ffe3-136">RELATED LINKS</span></span>

[<span data-ttu-id="4ffe3-137">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4ffe3-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="4ffe3-138">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4ffe3-138">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="4ffe3-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4ffe3-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="4ffe3-140">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4ffe3-140">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="4ffe3-141">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4ffe3-141">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="4ffe3-142">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4ffe3-142">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

