---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093174"
---
# <span data-ttu-id="8144e-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="8144e-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="8144e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8144e-102">SYNOPSIS</span></span>
<span data-ttu-id="8144e-103">Anger en resurs som den aktuella resursen.</span><span class="sxs-lookup"><span data-stu-id="8144e-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="8144e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8144e-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8144e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8144e-105">DESCRIPTION</span></span>
<span data-ttu-id="8144e-106">Cmdleten **Select-AzureStorSimpleResource** anger en resurs som den aktuella resursen.</span><span class="sxs-lookup"><span data-stu-id="8144e-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="8144e-107">När du har valt en resurs tillämpas andra cmdletar i den resurs kontexten.</span><span class="sxs-lookup"><span data-stu-id="8144e-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="8144e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8144e-108">EXAMPLES</span></span>

### <span data-ttu-id="8144e-109">Exempel 1: Välj en resurs för första gången</span><span class="sxs-lookup"><span data-stu-id="8144e-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="8144e-110">Det här kommandot väljer resursen som heter Contoso64-Tsqa som den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="8144e-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="8144e-111">I det här exemplet har datorn inte haft den här kontexten initierats tidigare och därför måste du ange ett värde för parametern *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="8144e-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="8144e-112">Exempel 2: försök att välja en resurs</span><span class="sxs-lookup"><span data-stu-id="8144e-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="8144e-113">Exempel 3: Välj en tidigare markerad resurs</span><span class="sxs-lookup"><span data-stu-id="8144e-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="8144e-114">Det här kommandot väljer resursen som heter Contoso64-Tsqa som den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="8144e-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="8144e-115">I det här exemplet har den här kontexten redan valts och därför behöver du inte ange ett värde för parametern *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="8144e-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="8144e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8144e-116">PARAMETERS</span></span>

### <span data-ttu-id="8144e-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="8144e-117">-Profile</span></span>
<span data-ttu-id="8144e-118">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="8144e-118">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8144e-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="8144e-119">-RegistrationKey</span></span>
<span data-ttu-id="8144e-120">Anger en registrerings skylt.</span><span class="sxs-lookup"><span data-stu-id="8144e-120">Specifies a registration key.</span></span>
<span data-ttu-id="8144e-121">Ange en sessionsnyckel första gången du väljer en resurs.</span><span class="sxs-lookup"><span data-stu-id="8144e-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="8144e-122">När denna cmdlet väljer den aktuella resursen använder cmdletar den här tangenten, efter behov.</span><span class="sxs-lookup"><span data-stu-id="8144e-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="8144e-123">Mer information finns i [Hämta tjänste registrerings knappen](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) i Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="8144e-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="8144e-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8144e-124">-ResourceName</span></span>
<span data-ttu-id="8144e-125">Anger namnet på resursen som ska markeras som den aktuella resursen.</span><span class="sxs-lookup"><span data-stu-id="8144e-125">Specifies the name of the resource to select as the current resource.</span></span>

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

### <span data-ttu-id="8144e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8144e-126">CommonParameters</span></span>
<span data-ttu-id="8144e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8144e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8144e-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8144e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8144e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8144e-129">INPUTS</span></span>

### <span data-ttu-id="8144e-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="8144e-130">None</span></span>

## <span data-ttu-id="8144e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8144e-131">OUTPUTS</span></span>

### <span data-ttu-id="8144e-132">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="8144e-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="8144e-133">Denna cmdlet returnerar ett **StorSimpleResourceContext** -objekt som innehåller information om resurs kontexten.</span><span class="sxs-lookup"><span data-stu-id="8144e-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="8144e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8144e-134">NOTES</span></span>

## <span data-ttu-id="8144e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8144e-135">RELATED LINKS</span></span>

[<span data-ttu-id="8144e-136">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="8144e-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="8144e-137">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="8144e-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)


