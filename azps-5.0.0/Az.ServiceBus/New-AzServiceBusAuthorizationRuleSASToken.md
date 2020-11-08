---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: d314deb2515907b7d2b668d18d165a7fb0691509
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272690"
---
# <span data-ttu-id="6e3fd-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6e3fd-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="6e3fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3fd-103">Genererar en SAS-Tolen för Azure ServiceBus-auktoriseringsregel i namn område/kö/ämne.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="6e3fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e3fd-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e3fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e3fd-105">DESCRIPTION</span></span>
<span data-ttu-id="6e3fd-106">New-AzServiceBusAuthorizationRuleSASToken-cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Eventhub-Namesapce eller Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="6e3fd-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="6e3fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e3fd-107">EXAMPLES</span></span>

### <span data-ttu-id="6e3fd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6e3fd-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="6e3fd-109">Skapa SAS-token för den angivna authorixation regeln för namn område med start-och utgångs tid.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="6e3fd-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6e3fd-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="6e3fd-111">Skapa SAS-token för den angivna authorixation regeln för namn område med förfallo tid.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="6e3fd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e3fd-112">PARAMETERS</span></span>

### <span data-ttu-id="6e3fd-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="6e3fd-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="6e3fd-114">Authoraization-regelns ARM ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e3fd-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="6e3fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3fd-115">-DefaultProfile</span></span>
<span data-ttu-id="6e3fd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e3fd-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6e3fd-117">-ExpiryTime</span></span>
<span data-ttu-id="6e3fd-118">Förfallo tid</span><span class="sxs-lookup"><span data-stu-id="6e3fd-118">Expiry Time</span></span>

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

### <span data-ttu-id="6e3fd-119">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="6e3fd-119">-KeyType</span></span>
<span data-ttu-id="6e3fd-120">Typ av knapp</span><span class="sxs-lookup"><span data-stu-id="6e3fd-120">Key Type</span></span>

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

### <span data-ttu-id="6e3fd-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6e3fd-121">-StartTime</span></span>
<span data-ttu-id="6e3fd-122">Start tid</span><span class="sxs-lookup"><span data-stu-id="6e3fd-122">Start Time</span></span>

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

### <span data-ttu-id="6e3fd-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6e3fd-123">-Confirm</span></span>
<span data-ttu-id="6e3fd-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e3fd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e3fd-125">-WhatIf</span></span>
<span data-ttu-id="6e3fd-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e3fd-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e3fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3fd-128">CommonParameters</span></span>
<span data-ttu-id="6e3fd-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6e3fd-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e3fd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3fd-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e3fd-131">INPUTS</span></span>

### <span data-ttu-id="6e3fd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6e3fd-132">System.String</span></span>

### <span data-ttu-id="6e3fd-133">System. Nullable ' 1 [[system. DateTime, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6e3fd-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6e3fd-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e3fd-134">OUTPUTS</span></span>

### <span data-ttu-id="6e3fd-135">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="6e3fd-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="6e3fd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e3fd-136">NOTES</span></span>

## <span data-ttu-id="6e3fd-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e3fd-137">RELATED LINKS</span></span>