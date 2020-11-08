---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 7e1bf5552d8c6fd6c7dff0c4478557059b0bc78a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089576"
---
# <span data-ttu-id="b71ad-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b71ad-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="b71ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b71ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b71ad-103">Aktiverar principen för avancerat skydd för en lagrings-cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b71ad-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="b71ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b71ad-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b71ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b71ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b71ad-106">`Enable-AzSecurityAdvancedThreatProtection`Cmdleten aktiverar hot skydds principen för ett lagrings-cosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="b71ad-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="b71ad-107">Ange parametern *ResourceID* för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b71ad-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="b71ad-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b71ad-108">EXAMPLES</span></span>

### <span data-ttu-id="b71ad-109">Exempel 1: lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b71ad-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="b71ad-110">Det här kommandot aktiverar principen för avancerat skydd för resurs-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="b71ad-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="b71ad-111">Exempel 2: CosmosDB-konto</span><span class="sxs-lookup"><span data-stu-id="b71ad-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="b71ad-112">Det här kommandot aktiverar principen för avancerat skydd för resurs-ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="b71ad-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="b71ad-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b71ad-113">PARAMETERS</span></span>

### <span data-ttu-id="b71ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71ad-114">-DefaultProfile</span></span>
<span data-ttu-id="b71ad-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b71ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b71ad-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b71ad-116">-ResourceId</span></span>
<span data-ttu-id="b71ad-117">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="b71ad-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b71ad-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b71ad-118">-Confirm</span></span>
<span data-ttu-id="b71ad-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b71ad-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b71ad-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b71ad-120">-WhatIf</span></span>
<span data-ttu-id="b71ad-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b71ad-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b71ad-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b71ad-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b71ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71ad-123">CommonParameters</span></span>
<span data-ttu-id="b71ad-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71ad-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b71ad-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71ad-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b71ad-126">INPUTS</span></span>

### <span data-ttu-id="b71ad-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="b71ad-127">None</span></span>

## <span data-ttu-id="b71ad-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b71ad-128">OUTPUTS</span></span>

### <span data-ttu-id="b71ad-129">Microsoft. Azure. commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b71ad-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="b71ad-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b71ad-130">NOTES</span></span>

## <span data-ttu-id="b71ad-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b71ad-131">RELATED LINKS</span></span>