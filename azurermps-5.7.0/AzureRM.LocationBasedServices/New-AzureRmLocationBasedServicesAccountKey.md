---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 7116cd4c5da2dd897af4e6540593a5e5458e4eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576496"
---
# <span data-ttu-id="0160a-101">New-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="0160a-101">New-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="0160a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0160a-102">SYNOPSIS</span></span>
<span data-ttu-id="0160a-103">Återskapar en konto-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="0160a-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0160a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0160a-104">SYNTAX</span></span>

### <span data-ttu-id="0160a-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0160a-105">NameParameterSet (Default)</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0160a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0160a-106">InputObjectParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0160a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0160a-107">ResourceIdParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0160a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0160a-108">DESCRIPTION</span></span>
<span data-ttu-id="0160a-109">**New-AzureRmLocationBasedServicesAccountKey** cmdlet återskapar en API-nyckeln för ett platsbaserade tjänst konto.</span><span class="sxs-lookup"><span data-stu-id="0160a-109">The **New-AzureRmLocationBasedServicesAccountKey** cmdlet regenerates an API key for a Location Based Services account.</span></span>

## <span data-ttu-id="0160a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0160a-110">EXAMPLES</span></span>

### <span data-ttu-id="0160a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0160a-111">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="0160a-112">Återskapar den primära API-nyckeln för konto-ID i resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0160a-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="0160a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0160a-113">Example 2</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="0160a-114">Återskapar den sekundära API-nyckeln för det angivna platsbaserade tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="0160a-114">Regenerates the Secondary API Key for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="0160a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0160a-115">PARAMETERS</span></span>

### <span data-ttu-id="0160a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0160a-116">-DefaultProfile</span></span>
<span data-ttu-id="0160a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0160a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0160a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0160a-118">-InputObject</span></span>
<span data-ttu-id="0160a-119">Piped från [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="0160a-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

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

### <span data-ttu-id="0160a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0160a-120">-KeyName</span></span>
<span data-ttu-id="0160a-121">Konto nycklar för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="0160a-121">Location Based Services Account Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0160a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0160a-122">-Name</span></span>
<span data-ttu-id="0160a-123">Konto namn för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="0160a-123">Location Based Services Account Name.</span></span>

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

### <span data-ttu-id="0160a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0160a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0160a-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="0160a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="0160a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0160a-126">-ResourceId</span></span>
<span data-ttu-id="0160a-127">Platsbaserade tjänst konton ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0160a-127">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="0160a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0160a-128">-Confirm</span></span>
<span data-ttu-id="0160a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0160a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0160a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0160a-130">-WhatIf</span></span>
<span data-ttu-id="0160a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0160a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0160a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0160a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0160a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0160a-133">CommonParameters</span></span>
<span data-ttu-id="0160a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0160a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0160a-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0160a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0160a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0160a-136">INPUTS</span></span>

### <span data-ttu-id="0160a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0160a-137">System.String</span></span>
<span data-ttu-id="0160a-138">Microsoft. Azure. commands. LocationBasedServices. NewAzureLocationBasedServicesAccountKeyCommand + KeyNameType</span><span class="sxs-lookup"><span data-stu-id="0160a-138">Microsoft.Azure.Commands.LocationBasedServices.NewAzureLocationBasedServicesAccountKeyCommand+KeyNameType</span></span>

## <span data-ttu-id="0160a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0160a-139">OUTPUTS</span></span>

### <span data-ttu-id="0160a-140">Microsoft. Azure. Management. LocationBasedServices. Models. LocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0160a-140">Microsoft.Azure.Management.LocationBasedServices.Models.LocationBasedServicesAccountKeys</span></span>

## <span data-ttu-id="0160a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0160a-141">NOTES</span></span>

## <span data-ttu-id="0160a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0160a-142">RELATED LINKS</span></span>
