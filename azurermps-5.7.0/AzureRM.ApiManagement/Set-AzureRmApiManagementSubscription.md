---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 62c1bd394dd509b81a8ea748c26c0465718926c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583703"
---
# <span data-ttu-id="4c950-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c950-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="4c950-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c950-102">SYNOPSIS</span></span>
<span data-ttu-id="4c950-103">Anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="4c950-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c950-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c950-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c950-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c950-105">DESCRIPTION</span></span>
<span data-ttu-id="4c950-106">Cmdleten **set-AzureRmApiManagementSubscription** anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="4c950-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="4c950-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c950-107">EXAMPLES</span></span>

### <span data-ttu-id="4c950-108">Exempel 1: Ange tillstånd och primär-och sekundär nycklar för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="4c950-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="4c950-109">Det här kommandot anger de primära och sekundära nycklarna för ett abonnemang och aktiverar det.</span><span class="sxs-lookup"><span data-stu-id="4c950-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="4c950-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c950-110">PARAMETERS</span></span>

### <span data-ttu-id="4c950-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4c950-111">-Context</span></span>
<span data-ttu-id="4c950-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4c950-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4c950-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c950-113">-DefaultProfile</span></span>
<span data-ttu-id="4c950-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c950-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4c950-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="4c950-115">-ExpiresOn</span></span>
<span data-ttu-id="4c950-116">Anger ett förfallo datum för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4c950-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="4c950-117">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="4c950-117">The default value of this parameter is $Null.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c950-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c950-118">-Name</span></span>
<span data-ttu-id="4c950-119">Anger ett prenumerations namn.</span><span class="sxs-lookup"><span data-stu-id="4c950-119">Specifies a subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c950-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c950-120">-PassThru</span></span>
<span data-ttu-id="4c950-121">passthru</span><span class="sxs-lookup"><span data-stu-id="4c950-121">passthru</span></span>

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

### <span data-ttu-id="4c950-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4c950-122">-PrimaryKey</span></span>
<span data-ttu-id="4c950-123">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4c950-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="4c950-124">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="4c950-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="4c950-125">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="4c950-125">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c950-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4c950-126">-SecondaryKey</span></span>
<span data-ttu-id="4c950-127">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="4c950-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="4c950-128">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="4c950-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="4c950-129">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="4c950-129">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c950-130">-State</span><span class="sxs-lookup"><span data-stu-id="4c950-130">-State</span></span>
<span data-ttu-id="4c950-131">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4c950-131">Specifies the subscription state.</span></span>
<span data-ttu-id="4c950-132">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="4c950-132">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c950-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="4c950-133">-StateComment</span></span>
<span data-ttu-id="4c950-134">Anger kommentaren till abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4c950-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="4c950-135">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="4c950-135">The default value of this parameter is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c950-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c950-136">-SubscriptionId</span></span>
<span data-ttu-id="4c950-137">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="4c950-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="4c950-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c950-138">CommonParameters</span></span>
<span data-ttu-id="4c950-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c950-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c950-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c950-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c950-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c950-141">INPUTS</span></span>

### <span data-ttu-id="4c950-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="4c950-142">None</span></span>
<span data-ttu-id="4c950-143">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4c950-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c950-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c950-144">OUTPUTS</span></span>

### <span data-ttu-id="4c950-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="4c950-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="4c950-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c950-146">NOTES</span></span>

## <span data-ttu-id="4c950-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c950-147">RELATED LINKS</span></span>

[<span data-ttu-id="4c950-148">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c950-148">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="4c950-149">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c950-149">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="4c950-150">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c950-150">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


