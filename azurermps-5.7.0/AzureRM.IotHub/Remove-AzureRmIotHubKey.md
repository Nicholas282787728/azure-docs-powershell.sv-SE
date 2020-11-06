---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 4f1c21f4f64193ec25a0392e094b8fd492ceba9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576504"
---
# <span data-ttu-id="43a14-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="43a14-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="43a14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43a14-102">SYNOPSIS</span></span>
<span data-ttu-id="43a14-103">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="43a14-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43a14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43a14-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43a14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43a14-105">DESCRIPTION</span></span>
<span data-ttu-id="43a14-106">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="43a14-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="43a14-107">Om det finns flera tangenter med samma namn tas den första i listan bort.</span><span class="sxs-lookup"><span data-stu-id="43a14-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="43a14-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43a14-108">EXAMPLES</span></span>

### <span data-ttu-id="43a14-109">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="43a14-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="43a14-110">Tar bort den iothubowner1 från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="43a14-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="43a14-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43a14-111">PARAMETERS</span></span>

### <span data-ttu-id="43a14-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a14-112">-DefaultProfile</span></span>
<span data-ttu-id="43a14-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="43a14-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43a14-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="43a14-114">-KeyName</span></span>
<span data-ttu-id="43a14-115">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="43a14-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a14-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="43a14-116">-Name</span></span>
<span data-ttu-id="43a14-117">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="43a14-117">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a14-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a14-118">-ResourceGroupName</span></span>
<span data-ttu-id="43a14-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="43a14-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a14-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43a14-120">-Confirm</span></span>
<span data-ttu-id="43a14-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43a14-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a14-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a14-122">-WhatIf</span></span>
<span data-ttu-id="43a14-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43a14-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43a14-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43a14-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a14-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a14-125">CommonParameters</span></span>
<span data-ttu-id="43a14-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a14-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a14-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a14-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a14-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43a14-128">INPUTS</span></span>

### <span data-ttu-id="43a14-129">System. String</span><span class="sxs-lookup"><span data-stu-id="43a14-129">System.String</span></span>

## <span data-ttu-id="43a14-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43a14-130">OUTPUTS</span></span>

### <span data-ttu-id="43a14-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="43a14-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="43a14-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43a14-132">NOTES</span></span>

## <span data-ttu-id="43a14-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43a14-133">RELATED LINKS</span></span>

