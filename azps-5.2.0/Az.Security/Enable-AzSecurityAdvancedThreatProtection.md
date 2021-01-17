---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396136"
---
# <span data-ttu-id="2f3f4-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2f3f4-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="2f3f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f3f4-103">Aktiverar principen för avancerat skydd för en lagrings-cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="2f3f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f3f4-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f3f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f3f4-105">DESCRIPTION</span></span>
<span data-ttu-id="2f3f4-106">`Enable-AzSecurityAdvancedThreatProtection`Cmdleten aktiverar hot skydds principen för ett lagrings-cosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="2f3f4-107">Ange parametern *ResourceID* för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="2f3f4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f3f4-108">EXAMPLES</span></span>

### <span data-ttu-id="2f3f4-109">Exempel 1: lagrings konto</span><span class="sxs-lookup"><span data-stu-id="2f3f4-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="2f3f4-110">Det här kommandot aktiverar principen för avancerat skydd för resurs-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="2f3f4-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="2f3f4-111">Exempel 2: CosmosDB-konto</span><span class="sxs-lookup"><span data-stu-id="2f3f4-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="2f3f4-112">Det här kommandot aktiverar principen för avancerat skydd för resurs-ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="2f3f4-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="2f3f4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f3f4-113">PARAMETERS</span></span>

### <span data-ttu-id="2f3f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f3f4-114">-DefaultProfile</span></span>
<span data-ttu-id="2f3f4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f3f4-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f3f4-116">-ResourceId</span></span>
<span data-ttu-id="2f3f4-117">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2f3f4-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f3f4-118">-Confirm</span></span>
<span data-ttu-id="2f3f4-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f3f4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f3f4-120">-WhatIf</span></span>
<span data-ttu-id="2f3f4-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f3f4-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f3f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3f4-123">CommonParameters</span></span>
<span data-ttu-id="2f3f4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3f4-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f3f4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3f4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f3f4-126">INPUTS</span></span>

### <span data-ttu-id="2f3f4-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="2f3f4-127">None</span></span>

## <span data-ttu-id="2f3f4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f3f4-128">OUTPUTS</span></span>

### <span data-ttu-id="2f3f4-129">Microsoft. Azure. commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2f3f4-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="2f3f4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f3f4-130">NOTES</span></span>

## <span data-ttu-id="2f3f4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f3f4-131">RELATED LINKS</span></span>
