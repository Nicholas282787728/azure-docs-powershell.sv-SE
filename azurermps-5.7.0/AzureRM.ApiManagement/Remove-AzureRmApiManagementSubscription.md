---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 777d71dec17f75cba84c15c7499e5ec56ffb854a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758355"
---
# <span data-ttu-id="e9571-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e9571-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="e9571-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9571-102">SYNOPSIS</span></span>
<span data-ttu-id="e9571-103">Tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e9571-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9571-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9571-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9571-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9571-105">DESCRIPTION</span></span>
<span data-ttu-id="e9571-106">Cmdleten **Remove-AzureRmApiManagementSubscription** tar bort en befintlig prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e9571-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="e9571-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9571-107">EXAMPLES</span></span>

### <span data-ttu-id="e9571-108">Exempel 1: ta bort ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="e9571-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="e9571-109">Det här kommandot tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e9571-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="e9571-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9571-110">PARAMETERS</span></span>

### <span data-ttu-id="e9571-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e9571-111">-Context</span></span>
<span data-ttu-id="e9571-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e9571-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9571-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9571-113">-DefaultProfile</span></span>
<span data-ttu-id="e9571-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9571-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e9571-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9571-115">-PassThru</span></span>
<span data-ttu-id="e9571-116">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $false värde.</span><span class="sxs-lookup"><span data-stu-id="e9571-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9571-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9571-117">-SubscriptionId</span></span>
<span data-ttu-id="e9571-118">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="e9571-118">Specifies the subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9571-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9571-119">-Confirm</span></span>
<span data-ttu-id="e9571-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9571-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9571-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9571-121">-WhatIf</span></span>
<span data-ttu-id="e9571-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9571-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9571-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9571-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9571-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9571-124">CommonParameters</span></span>
<span data-ttu-id="e9571-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9571-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9571-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9571-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9571-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9571-127">INPUTS</span></span>

### <span data-ttu-id="e9571-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="e9571-128">None</span></span>
<span data-ttu-id="e9571-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e9571-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9571-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9571-130">OUTPUTS</span></span>

### <span data-ttu-id="e9571-131">Returtyp</span><span class="sxs-lookup"><span data-stu-id="e9571-131">Boolean</span></span>

## <span data-ttu-id="e9571-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9571-132">NOTES</span></span>

## <span data-ttu-id="e9571-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9571-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9571-134">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e9571-134">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="e9571-135">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e9571-135">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="e9571-136">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e9571-136">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


