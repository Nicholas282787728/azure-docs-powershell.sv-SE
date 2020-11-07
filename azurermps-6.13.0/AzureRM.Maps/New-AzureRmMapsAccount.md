---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
ms.openlocfilehash: 0b8bfad1b3bb9f24c6b7c74e92f64c64d776c2d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577935"
---
# <span data-ttu-id="c4d90-101">New-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c4d90-101">New-AzureRmMapsAccount</span></span>

## <span data-ttu-id="c4d90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4d90-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d90-103">Skapar ett Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="c4d90-103">Creates an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4d90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4d90-104">SYNTAX</span></span>

```
New-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d90-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4d90-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d90-106">New-AzureRmMapsAccount-cmdleten skapar ett Azure Maps-konto med angivet SKU.</span><span class="sxs-lookup"><span data-stu-id="c4d90-106">The New-AzureRmMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="c4d90-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4d90-107">EXAMPLES</span></span>

### <span data-ttu-id="c4d90-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4d90-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="c4d90-109">Skapar ett nytt Azure Maps-konto med namnet mitt konto i resurs gruppen MyResourceGroup med SKU-S0 och en-etikett.</span><span class="sxs-lookup"><span data-stu-id="c4d90-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="c4d90-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4d90-110">PARAMETERS</span></span>

### <span data-ttu-id="c4d90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d90-111">-DefaultProfile</span></span>
<span data-ttu-id="c4d90-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d90-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4d90-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c4d90-113">-Force</span></span>
<span data-ttu-id="c4d90-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c4d90-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c4d90-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4d90-115">-Name</span></span>
<span data-ttu-id="c4d90-116">Mappar konto namn.</span><span class="sxs-lookup"><span data-stu-id="c4d90-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="c4d90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d90-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4d90-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c4d90-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4d90-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c4d90-119">-SkuName</span></span>
<span data-ttu-id="c4d90-120">Mappar kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="c4d90-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d90-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c4d90-121">-Tag</span></span>
<span data-ttu-id="c4d90-122">Mappar konto koder.</span><span class="sxs-lookup"><span data-stu-id="c4d90-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="c4d90-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4d90-123">-Confirm</span></span>
<span data-ttu-id="c4d90-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4d90-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d90-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d90-125">-WhatIf</span></span>
<span data-ttu-id="c4d90-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4d90-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4d90-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4d90-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d90-128">CommonParameters</span></span>
<span data-ttu-id="c4d90-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d90-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d90-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d90-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4d90-131">INPUTS</span></span>

### <span data-ttu-id="c4d90-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d90-132">System.String</span></span>

## <span data-ttu-id="c4d90-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4d90-133">OUTPUTS</span></span>

### <span data-ttu-id="c4d90-134">Microsoft. Azure. commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c4d90-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="c4d90-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4d90-135">NOTES</span></span>

## <span data-ttu-id="c4d90-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4d90-136">RELATED LINKS</span></span>