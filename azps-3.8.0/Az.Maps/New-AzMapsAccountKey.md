---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: c115cd780750770e05bc55b1f70a7cfe33967fff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089802"
---
# <span data-ttu-id="b477a-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="b477a-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="b477a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b477a-102">SYNOPSIS</span></span>
<span data-ttu-id="b477a-103">Återskapar en konto-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="b477a-103">Regenerates an account key.</span></span>

## <span data-ttu-id="b477a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b477a-104">SYNTAX</span></span>

### <span data-ttu-id="b477a-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b477a-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b477a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b477a-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b477a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b477a-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b477a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b477a-108">DESCRIPTION</span></span>
<span data-ttu-id="b477a-109">New-AzMapsAccountKey cmdlet återskapar en API-nyckeln för ett Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="b477a-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="b477a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b477a-110">EXAMPLES</span></span>

### <span data-ttu-id="b477a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b477a-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="b477a-112">Återskapar den primära API-nyckeln för konto-ID i resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b477a-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b477a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b477a-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="b477a-114">Återskapar den sekundära API-nyckeln för det angivna Azure Maps-kontot.</span><span class="sxs-lookup"><span data-stu-id="b477a-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="b477a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b477a-115">PARAMETERS</span></span>

### <span data-ttu-id="b477a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b477a-116">-DefaultProfile</span></span>
<span data-ttu-id="b477a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b477a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b477a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b477a-118">-InputObject</span></span>
<span data-ttu-id="b477a-119">Mappar piped från get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="b477a-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="b477a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b477a-120">-KeyName</span></span>
<span data-ttu-id="b477a-121">Kopplar konto.</span><span class="sxs-lookup"><span data-stu-id="b477a-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b477a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b477a-122">-Name</span></span>
<span data-ttu-id="b477a-123">Mappar konto namn.</span><span class="sxs-lookup"><span data-stu-id="b477a-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="b477a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b477a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b477a-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b477a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b477a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b477a-126">-ResourceId</span></span>
<span data-ttu-id="b477a-127">Kopplar ihop konto-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b477a-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="b477a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b477a-128">-Confirm</span></span>
<span data-ttu-id="b477a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b477a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b477a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b477a-130">-WhatIf</span></span>
<span data-ttu-id="b477a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b477a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b477a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b477a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b477a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b477a-133">CommonParameters</span></span>
<span data-ttu-id="b477a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b477a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b477a-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b477a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b477a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b477a-136">INPUTS</span></span>

### <span data-ttu-id="b477a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b477a-137">System.String</span></span>

### <span data-ttu-id="b477a-138">Microsoft. Azure. commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b477a-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="b477a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b477a-139">OUTPUTS</span></span>

### <span data-ttu-id="b477a-140">Microsoft. Azure. Management. Maps. Models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b477a-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="b477a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b477a-141">NOTES</span></span>

## <span data-ttu-id="b477a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b477a-142">RELATED LINKS</span></span>