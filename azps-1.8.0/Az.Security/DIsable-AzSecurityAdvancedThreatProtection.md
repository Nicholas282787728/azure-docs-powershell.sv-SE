---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: a3e83b4c58a7de2a0c020bc156e78656a6fd75ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746991"
---
# <span data-ttu-id="e0066-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="e0066-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="e0066-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0066-102">SYNOPSIS</span></span>
<span data-ttu-id="e0066-103">Inaktiverar principen för avancerat skydd för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e0066-103">Disables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="e0066-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0066-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0066-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0066-105">DESCRIPTION</span></span>
<span data-ttu-id="e0066-106">Denna `Disable-AzSecurityAdvancedThreatProtection` cmdlet inaktiverar hotet protetion-principen för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e0066-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="e0066-107">Ange parametern *ResourceID* för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0066-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="e0066-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0066-108">EXAMPLES</span></span>

### <span data-ttu-id="e0066-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0066-109">Example 1</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="e0066-110">Det här kommandot inaktiverar principen för avancerat skydd för resurs-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="e0066-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="e0066-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0066-111">PARAMETERS</span></span>

### <span data-ttu-id="e0066-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0066-112">-DefaultProfile</span></span>
<span data-ttu-id="e0066-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0066-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0066-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0066-114">-ResourceId</span></span>
<span data-ttu-id="e0066-115">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="e0066-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e0066-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0066-116">-Confirm</span></span>
<span data-ttu-id="e0066-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0066-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0066-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0066-118">-WhatIf</span></span>
<span data-ttu-id="e0066-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0066-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0066-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0066-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0066-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0066-121">CommonParameters</span></span>
<span data-ttu-id="e0066-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0066-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0066-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0066-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0066-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0066-124">INPUTS</span></span>

### <span data-ttu-id="e0066-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="e0066-125">None</span></span>

## <span data-ttu-id="e0066-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0066-126">OUTPUTS</span></span>

### <span data-ttu-id="e0066-127">Microsoft. Azure. commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="e0066-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="e0066-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0066-128">NOTES</span></span>

## <span data-ttu-id="e0066-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0066-129">RELATED LINKS</span></span>
