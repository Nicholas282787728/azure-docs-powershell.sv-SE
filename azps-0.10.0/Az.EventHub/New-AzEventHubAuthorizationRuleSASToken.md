---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 85155804c128b67a77e458bb68f04155499ed31a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922905"
---
# <span data-ttu-id="74667-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="74667-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="74667-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74667-102">SYNOPSIS</span></span>
<span data-ttu-id="74667-103">Genererar en SAS-token för Azure eventhub-auktoriseringsregeln för namespace/eventhub.</span><span class="sxs-lookup"><span data-stu-id="74667-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="74667-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74667-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74667-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74667-105">DESCRIPTION</span></span>
<span data-ttu-id="74667-106">New-AzEventHubAuthorizationRuleSASToken-cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Eventhub-Namesapce eller Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="74667-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="74667-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74667-107">EXAMPLES</span></span>

### <span data-ttu-id="74667-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="74667-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="74667-109">Skapa SAS-token för den angivna authorixation regeln för namn område med start-och utgångs tid.</span><span class="sxs-lookup"><span data-stu-id="74667-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="74667-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="74667-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="74667-111">Skapa SAS-token för den angivna authorixation regeln för namn område med förfallo tid.</span><span class="sxs-lookup"><span data-stu-id="74667-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="74667-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74667-112">PARAMETERS</span></span>

### <span data-ttu-id="74667-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="74667-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="74667-114">Authoraization-regelns ARM ResourceId</span><span class="sxs-lookup"><span data-stu-id="74667-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74667-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74667-115">-DefaultProfile</span></span>
<span data-ttu-id="74667-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74667-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74667-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="74667-117">-ExpiryTime</span></span>
<span data-ttu-id="74667-118">Förfallo tid</span><span class="sxs-lookup"><span data-stu-id="74667-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74667-119">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="74667-119">-KeyType</span></span>
<span data-ttu-id="74667-120">Typ av knapp</span><span class="sxs-lookup"><span data-stu-id="74667-120">Key Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74667-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="74667-121">-StartTime</span></span>
<span data-ttu-id="74667-122">Start tid</span><span class="sxs-lookup"><span data-stu-id="74667-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74667-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74667-123">-Confirm</span></span>
<span data-ttu-id="74667-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74667-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74667-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74667-125">-WhatIf</span></span>
<span data-ttu-id="74667-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74667-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74667-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74667-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74667-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74667-128">CommonParameters</span></span>
<span data-ttu-id="74667-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74667-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="74667-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74667-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74667-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74667-131">INPUTS</span></span>

### <span data-ttu-id="74667-132">System. String</span><span class="sxs-lookup"><span data-stu-id="74667-132">System.String</span></span>

### <span data-ttu-id="74667-133">System. Nullable ' 1 [[system. DateTime, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="74667-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="74667-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74667-134">OUTPUTS</span></span>

### <span data-ttu-id="74667-135">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="74667-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="74667-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74667-136">NOTES</span></span>

## <span data-ttu-id="74667-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74667-137">RELATED LINKS</span></span>
