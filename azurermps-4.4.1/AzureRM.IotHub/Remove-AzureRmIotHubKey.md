---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 8b7603f145d45411b20b124823f28281d4117127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755450"
---
# <span data-ttu-id="b4b1c-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b4b1c-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="b4b1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b1c-103">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="b4b1c-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4b1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4b1c-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b1c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4b1c-105">DESCRIPTION</span></span>
<span data-ttu-id="b4b1c-106">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="b4b1c-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="b4b1c-107">Om det finns flera tangenter med samma namn tas den första i listan bort.</span><span class="sxs-lookup"><span data-stu-id="b4b1c-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="b4b1c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4b1c-108">EXAMPLES</span></span>

### <span data-ttu-id="b4b1c-109">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="b4b1c-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="b4b1c-110">Tar bort den iothubowner1 från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b4b1c-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b4b1c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4b1c-111">PARAMETERS</span></span>

### <span data-ttu-id="b4b1c-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4b1c-112">-KeyName</span></span>
<span data-ttu-id="b4b1c-113">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="b4b1c-113">Name of the Key</span></span>

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

### <span data-ttu-id="b4b1c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4b1c-114">-Name</span></span>
<span data-ttu-id="b4b1c-115">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="b4b1c-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="b4b1c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b1c-116">-ResourceGroupName</span></span>
<span data-ttu-id="b4b1c-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b4b1c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="b4b1c-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4b1c-118">-Confirm</span></span>
<span data-ttu-id="b4b1c-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4b1c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b1c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b1c-120">-WhatIf</span></span>
<span data-ttu-id="b4b1c-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4b1c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b1c-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4b1c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b1c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b1c-123">-DefaultProfile</span></span>
<span data-ttu-id="b4b1c-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b1c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b1c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b1c-125">CommonParameters</span></span>
<span data-ttu-id="b4b1c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b1c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b1c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b1c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b1c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4b1c-128">INPUTS</span></span>

### <span data-ttu-id="b4b1c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b1c-129">System.String</span></span>

## <span data-ttu-id="b4b1c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4b1c-130">OUTPUTS</span></span>

### <span data-ttu-id="b4b1c-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b4b1c-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b4b1c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4b1c-132">NOTES</span></span>

## <span data-ttu-id="b4b1c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4b1c-133">RELATED LINKS</span></span>

