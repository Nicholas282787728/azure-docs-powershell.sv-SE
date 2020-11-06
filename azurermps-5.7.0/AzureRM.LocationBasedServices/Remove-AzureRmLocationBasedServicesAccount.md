---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581152"
---
# <span data-ttu-id="6c0a1-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6c0a1-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="6c0a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0a1-103">Tar bort ett konto för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c0a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c0a1-104">SYNTAX</span></span>

### <span data-ttu-id="6c0a1-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6c0a1-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c0a1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c0a1-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c0a1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c0a1-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c0a1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c0a1-108">DESCRIPTION</span></span>
<span data-ttu-id="6c0a1-109">Cmdleten **Remove-AzureRmLocationBasedServicesAccount** tar bort det angivna platsbaserade tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="6c0a1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c0a1-110">EXAMPLES</span></span>

### <span data-ttu-id="6c0a1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6c0a1-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="6c0a1-112">Tar bort konto kontot från MyResourceGroup resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="6c0a1-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6c0a1-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="6c0a1-114">Tar bort det angivna platsbaserade tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="6c0a1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c0a1-115">PARAMETERS</span></span>

### <span data-ttu-id="6c0a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0a1-116">-DefaultProfile</span></span>
<span data-ttu-id="6c0a1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c0a1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c0a1-118">-InputObject</span></span>
<span data-ttu-id="6c0a1-119">Piped från [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="6c0a1-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0a1-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6c0a1-120">-Name</span></span>
<span data-ttu-id="6c0a1-121">Konto namn för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c0a1-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0a1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c0a1-124">-ResourceId</span></span>
<span data-ttu-id="6c0a1-125">Platsbaserade tjänst konton ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-125">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0a1-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6c0a1-126">-Confirm</span></span>
<span data-ttu-id="6c0a1-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0a1-128">-WhatIf</span></span>
<span data-ttu-id="6c0a1-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0a1-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0a1-131">CommonParameters</span></span>
<span data-ttu-id="6c0a1-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c0a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0a1-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0a1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0a1-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c0a1-134">INPUTS</span></span>

### <span data-ttu-id="6c0a1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6c0a1-135">System.String</span></span>

## <span data-ttu-id="6c0a1-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c0a1-136">OUTPUTS</span></span>

### <span data-ttu-id="6c0a1-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="6c0a1-137">System.Object</span></span>

## <span data-ttu-id="6c0a1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c0a1-138">NOTES</span></span>

## <span data-ttu-id="6c0a1-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c0a1-139">RELATED LINKS</span></span>
