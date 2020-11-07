---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 66731d988eb0232e4223343349bec05e5a12d44b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915797"
---
# <span data-ttu-id="1fcbc-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1fcbc-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="1fcbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fcbc-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcbc-103">Skapar ett Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="1fcbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fcbc-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fcbc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fcbc-105">DESCRIPTION</span></span>
<span data-ttu-id="1fcbc-106">New-AzMapsAccount-cmdleten skapar ett Azure Maps-konto med angivet SKU.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="1fcbc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fcbc-107">EXAMPLES</span></span>

### <span data-ttu-id="1fcbc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1fcbc-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="1fcbc-109">Skapar ett nytt Azure Maps-konto med namnet mitt konto i resurs gruppen MyResourceGroup med SKU-S0 och en-etikett.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="1fcbc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fcbc-110">PARAMETERS</span></span>

### <span data-ttu-id="1fcbc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcbc-111">-DefaultProfile</span></span>
<span data-ttu-id="1fcbc-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fcbc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1fcbc-113">-Force</span></span>
<span data-ttu-id="1fcbc-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1fcbc-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fcbc-115">-Name</span></span>
<span data-ttu-id="1fcbc-116">Mappar konto namn.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcbc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcbc-117">-ResourceGroupName</span></span>
<span data-ttu-id="1fcbc-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcbc-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1fcbc-119">-SkuName</span></span>
<span data-ttu-id="1fcbc-120">Mappar kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcbc-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1fcbc-121">-Tag</span></span>
<span data-ttu-id="1fcbc-122">Mappar konto koder.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcbc-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1fcbc-123">-Confirm</span></span>
<span data-ttu-id="1fcbc-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcbc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcbc-125">-WhatIf</span></span>
<span data-ttu-id="1fcbc-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fcbc-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcbc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcbc-128">CommonParameters</span></span>
<span data-ttu-id="1fcbc-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fcbc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcbc-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fcbc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcbc-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fcbc-131">INPUTS</span></span>

### <span data-ttu-id="1fcbc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1fcbc-132">System.String</span></span>

## <span data-ttu-id="1fcbc-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fcbc-133">OUTPUTS</span></span>

### <span data-ttu-id="1fcbc-134">Microsoft. Azure. commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1fcbc-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="1fcbc-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fcbc-135">NOTES</span></span>

## <span data-ttu-id="1fcbc-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fcbc-136">RELATED LINKS</span></span>
