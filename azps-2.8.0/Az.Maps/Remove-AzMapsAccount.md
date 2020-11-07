---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: ba474ca3ea3a975262eec8b98df1fb99b0f336cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743640"
---
# <span data-ttu-id="11522-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="11522-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="11522-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11522-102">SYNOPSIS</span></span>
<span data-ttu-id="11522-103">Tar bort ett Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="11522-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="11522-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11522-104">SYNTAX</span></span>

### <span data-ttu-id="11522-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="11522-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11522-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11522-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11522-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11522-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11522-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11522-108">DESCRIPTION</span></span>
<span data-ttu-id="11522-109">Remove-AzMapsAccount cmdlet tar bort angivet Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="11522-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="11522-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11522-110">EXAMPLES</span></span>

### <span data-ttu-id="11522-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="11522-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="11522-112">Tar bort konto kontot från MyResourceGroup resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="11522-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="11522-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="11522-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="11522-114">Tar bort angivet Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="11522-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="11522-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11522-115">PARAMETERS</span></span>

### <span data-ttu-id="11522-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11522-116">-DefaultProfile</span></span>
<span data-ttu-id="11522-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11522-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11522-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11522-118">-InputObject</span></span>
<span data-ttu-id="11522-119">Mappar piped från get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="11522-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="11522-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="11522-120">-Name</span></span>
<span data-ttu-id="11522-121">Mappar konto namn.</span><span class="sxs-lookup"><span data-stu-id="11522-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="11522-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11522-122">-PassThru</span></span>
<span data-ttu-id="11522-123">Returnera om det angivna kontot har tagits bort eller inte.</span><span class="sxs-lookup"><span data-stu-id="11522-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="11522-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11522-124">-ResourceGroupName</span></span>
<span data-ttu-id="11522-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="11522-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="11522-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11522-126">-ResourceId</span></span>
<span data-ttu-id="11522-127">Kopplar ihop konto-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="11522-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="11522-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11522-128">-Confirm</span></span>
<span data-ttu-id="11522-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11522-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11522-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11522-130">-WhatIf</span></span>
<span data-ttu-id="11522-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11522-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11522-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11522-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11522-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11522-133">CommonParameters</span></span>
<span data-ttu-id="11522-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11522-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11522-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11522-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11522-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11522-136">INPUTS</span></span>

### <span data-ttu-id="11522-137">System. String</span><span class="sxs-lookup"><span data-stu-id="11522-137">System.String</span></span>

### <span data-ttu-id="11522-138">Microsoft. Azure. commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="11522-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="11522-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11522-139">OUTPUTS</span></span>

### <span data-ttu-id="11522-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11522-140">System.Boolean</span></span>

## <span data-ttu-id="11522-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11522-141">NOTES</span></span>

## <span data-ttu-id="11522-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11522-142">RELATED LINKS</span></span>
