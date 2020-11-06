---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/remove-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
ms.openlocfilehash: 9880bf574aec57796d185742b2f33b79da8f7c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574832"
---
# <span data-ttu-id="1fc49-101">Remove-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1fc49-101">Remove-AzureRmMapsAccount</span></span>

## <span data-ttu-id="1fc49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fc49-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc49-103">Tar bort ett Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="1fc49-103">Deletes an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fc49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fc49-104">SYNTAX</span></span>

### <span data-ttu-id="1fc49-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1fc49-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fc49-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fc49-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fc49-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fc49-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fc49-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fc49-108">DESCRIPTION</span></span>
<span data-ttu-id="1fc49-109">Remove-AzureRmMapsAccount cmdlet tar bort angivet Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="1fc49-109">The Remove-AzureRmMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="1fc49-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fc49-110">EXAMPLES</span></span>

### <span data-ttu-id="1fc49-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1fc49-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="1fc49-112">Tar bort konto kontot från MyResourceGroup resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1fc49-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1fc49-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1fc49-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="1fc49-114">Tar bort angivet Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="1fc49-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="1fc49-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fc49-115">PARAMETERS</span></span>

### <span data-ttu-id="1fc49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc49-116">-DefaultProfile</span></span>
<span data-ttu-id="1fc49-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fc49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fc49-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fc49-118">-InputObject</span></span>
<span data-ttu-id="1fc49-119">Mappar piped från get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="1fc49-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc49-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fc49-120">-Name</span></span>
<span data-ttu-id="1fc49-121">Mappar konto namn.</span><span class="sxs-lookup"><span data-stu-id="1fc49-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc49-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fc49-122">-PassThru</span></span>
<span data-ttu-id="1fc49-123">Returnera om det angivna kontot har tagits bort eller inte.</span><span class="sxs-lookup"><span data-stu-id="1fc49-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="1fc49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc49-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fc49-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1fc49-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc49-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fc49-126">-ResourceId</span></span>
<span data-ttu-id="1fc49-127">Kopplar ihop konto-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1fc49-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc49-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1fc49-128">-Confirm</span></span>
<span data-ttu-id="1fc49-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fc49-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc49-130">-WhatIf</span></span>
<span data-ttu-id="1fc49-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1fc49-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fc49-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1fc49-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc49-133">CommonParameters</span></span>
<span data-ttu-id="1fc49-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc49-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc49-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc49-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fc49-136">INPUTS</span></span>

### <span data-ttu-id="1fc49-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1fc49-137">System.String</span></span>

### <span data-ttu-id="1fc49-138">Microsoft. Azure. commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1fc49-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="1fc49-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1fc49-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1fc49-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fc49-140">OUTPUTS</span></span>

### <span data-ttu-id="1fc49-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fc49-141">System.Boolean</span></span>

## <span data-ttu-id="1fc49-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fc49-142">NOTES</span></span>

## <span data-ttu-id="1fc49-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fc49-143">RELATED LINKS</span></span>
