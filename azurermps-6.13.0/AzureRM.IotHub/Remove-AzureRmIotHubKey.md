---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 0f48bf7ad03dcfd59f8ea3653acdb7a57aa5240c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574848"
---
# <span data-ttu-id="af444-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="af444-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="af444-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af444-102">SYNOPSIS</span></span>
<span data-ttu-id="af444-103">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="af444-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af444-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af444-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af444-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af444-105">DESCRIPTION</span></span>
<span data-ttu-id="af444-106">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="af444-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="af444-107">Om det finns flera tangenter med samma namn tas den första i listan bort.</span><span class="sxs-lookup"><span data-stu-id="af444-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="af444-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af444-108">EXAMPLES</span></span>

### <span data-ttu-id="af444-109">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="af444-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="af444-110">Tar bort den iothubowner1 från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="af444-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="af444-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af444-111">PARAMETERS</span></span>

### <span data-ttu-id="af444-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af444-112">-DefaultProfile</span></span>
<span data-ttu-id="af444-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="af444-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af444-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="af444-114">-KeyName</span></span>
<span data-ttu-id="af444-115">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="af444-115">Name of the Key</span></span>

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

### <span data-ttu-id="af444-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="af444-116">-Name</span></span>
<span data-ttu-id="af444-117">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="af444-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="af444-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af444-118">-ResourceGroupName</span></span>
<span data-ttu-id="af444-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="af444-119">Resource Group Name</span></span>

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

### <span data-ttu-id="af444-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af444-120">-Confirm</span></span>
<span data-ttu-id="af444-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af444-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af444-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af444-122">-WhatIf</span></span>
<span data-ttu-id="af444-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af444-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af444-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af444-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af444-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af444-125">CommonParameters</span></span>
<span data-ttu-id="af444-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af444-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af444-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af444-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af444-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af444-128">INPUTS</span></span>

### <span data-ttu-id="af444-129">System. String</span><span class="sxs-lookup"><span data-stu-id="af444-129">System.String</span></span>

## <span data-ttu-id="af444-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af444-130">OUTPUTS</span></span>

### <span data-ttu-id="af444-131">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="af444-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="af444-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af444-132">NOTES</span></span>

## <span data-ttu-id="af444-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af444-133">RELATED LINKS</span></span>
