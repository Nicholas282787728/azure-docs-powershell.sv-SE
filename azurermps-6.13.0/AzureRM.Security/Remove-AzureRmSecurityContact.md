---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581651"
---
# <span data-ttu-id="2bd1c-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="2bd1c-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="2bd1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd1c-103">Tar bort en säkerhets kontakt.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bd1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bd1c-104">SYNTAX</span></span>

### <span data-ttu-id="2bd1c-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="2bd1c-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-106">ID</span><span class="sxs-lookup"><span data-stu-id="2bd1c-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2bd1c-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd1c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bd1c-108">DESCRIPTION</span></span>
<span data-ttu-id="2bd1c-109">Tar bort en säkerhets kontakt.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-109">Deletes a security contact.</span></span>

## <span data-ttu-id="2bd1c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bd1c-110">EXAMPLES</span></span>

### <span data-ttu-id="2bd1c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2bd1c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="2bd1c-112">Tar bort säkerhets kontakten "default1"</span><span class="sxs-lookup"><span data-stu-id="2bd1c-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="2bd1c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bd1c-113">PARAMETERS</span></span>

### <span data-ttu-id="2bd1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd1c-114">-DefaultProfile</span></span>
<span data-ttu-id="2bd1c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bd1c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bd1c-116">-InputObject</span></span>
<span data-ttu-id="2bd1c-117">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd1c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2bd1c-118">-Name</span></span>
<span data-ttu-id="2bd1c-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd1c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bd1c-120">-PassThru</span></span>
<span data-ttu-id="2bd1c-121">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-121">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd1c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd1c-122">-ResourceId</span></span>
<span data-ttu-id="2bd1c-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-123">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd1c-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2bd1c-124">-Confirm</span></span>
<span data-ttu-id="2bd1c-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd1c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd1c-126">-WhatIf</span></span>
<span data-ttu-id="2bd1c-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bd1c-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd1c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd1c-129">CommonParameters</span></span>
<span data-ttu-id="2bd1c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd1c-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd1c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd1c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bd1c-132">INPUTS</span></span>

### <span data-ttu-id="2bd1c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2bd1c-133">System.String</span></span>
<span data-ttu-id="2bd1c-134">Microsoft. Azure. kommandon. Security. cmdletar. SecurityContacts. PSRemoveSecurityContactInputObject</span><span class="sxs-lookup"><span data-stu-id="2bd1c-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="2bd1c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bd1c-135">OUTPUTS</span></span>

### <span data-ttu-id="2bd1c-136">Microsoft. Azure. commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="2bd1c-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="2bd1c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bd1c-137">NOTES</span></span>

## <span data-ttu-id="2bd1c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bd1c-138">RELATED LINKS</span></span>
