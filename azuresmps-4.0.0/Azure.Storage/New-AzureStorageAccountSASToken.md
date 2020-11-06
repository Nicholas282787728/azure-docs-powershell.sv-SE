---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572339"
---
# <span data-ttu-id="25780-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="25780-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="25780-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25780-102">SYNOPSIS</span></span>
<span data-ttu-id="25780-103">Skapar en SAS-token.</span><span class="sxs-lookup"><span data-stu-id="25780-103">Creates an SAS token.</span></span>

## <span data-ttu-id="25780-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25780-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="25780-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25780-105">DESCRIPTION</span></span>
<span data-ttu-id="25780-106">Cmdleten **New-AzureStorageSASToken** skapar en SAS-token för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="25780-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="25780-107">Du kan använda SAS-token för att delegera behörigheter för flera tjänster eller för att delegera behörigheter för tjänster som inte är tillgängliga med en SAS-token på objekt nivå.</span><span class="sxs-lookup"><span data-stu-id="25780-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="25780-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25780-108">EXAMPLES</span></span>

### <span data-ttu-id="25780-109">Exempel 1: skapa en SAS-token</span><span class="sxs-lookup"><span data-stu-id="25780-109">Example 1: Create an SAS token</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="25780-110">Det här kommandot skapar en SAS-token på konto nivå med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="25780-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="25780-111">Exempel 2: skapa en SAS-token för ett intervall med IP-adresser</span><span class="sxs-lookup"><span data-stu-id="25780-111">Example 2: Create an SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="25780-112">Det här kommandot skapar en SAS-token för HTTPS-Only-begäranden från det angivna IP-adressintervallet.</span><span class="sxs-lookup"><span data-stu-id="25780-112">This command creates an SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="25780-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25780-113">PARAMETERS</span></span>

### <span data-ttu-id="25780-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="25780-114">-Context</span></span>
<span data-ttu-id="25780-115">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="25780-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="25780-116">Du kan använda New-AzureStorageContext cmdlet för att hämta ett **AzureStorageContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="25780-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25780-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="25780-117">-ExpiryTime</span></span>
<span data-ttu-id="25780-118">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="25780-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25780-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="25780-119">-IPAddressOrRange</span></span>
<span data-ttu-id="25780-120">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="25780-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="25780-121">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="25780-121">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25780-122">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="25780-122">-Permission</span></span>
<span data-ttu-id="25780-123">Anger behörigheterna för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="25780-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="25780-124">Behörigheter är bara giltiga om de stämmer överens med den angivna resurs typen.</span><span class="sxs-lookup"><span data-stu-id="25780-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="25780-125">Mer information om acceptabla behörighets värden finns i skapa en konto-SÄKERHETSASSOCIATIONERhttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="25780-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25780-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="25780-126">-Protocol</span></span>
<span data-ttu-id="25780-127">Anger det protokoll som tillåts för en begäran som gjorts med konto säkerhets associationen.</span><span class="sxs-lookup"><span data-stu-id="25780-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="25780-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="25780-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25780-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="25780-129">HttpsOnly</span></span>
- <span data-ttu-id="25780-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="25780-130">HttpsOrHttp</span></span>

<span data-ttu-id="25780-131">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="25780-131">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25780-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="25780-132">-ResourceType</span></span>
<span data-ttu-id="25780-133">Anger vilka resurs typer som är tillgängliga med SAS-token.</span><span class="sxs-lookup"><span data-stu-id="25780-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="25780-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="25780-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25780-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="25780-135">None</span></span>
- <span data-ttu-id="25780-136">Serv</span><span class="sxs-lookup"><span data-stu-id="25780-136">Service</span></span>
- <span data-ttu-id="25780-137">Beh</span><span class="sxs-lookup"><span data-stu-id="25780-137">Container</span></span>
- <span data-ttu-id="25780-138">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="25780-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25780-139">-Service</span><span class="sxs-lookup"><span data-stu-id="25780-139">-Service</span></span>
<span data-ttu-id="25780-140">Anger tjänsten.</span><span class="sxs-lookup"><span data-stu-id="25780-140">Specifies the service.</span></span>
<span data-ttu-id="25780-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="25780-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25780-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="25780-142">None</span></span>
- <span data-ttu-id="25780-143">Object</span><span class="sxs-lookup"><span data-stu-id="25780-143">Blob</span></span>
- <span data-ttu-id="25780-144">Fil</span><span class="sxs-lookup"><span data-stu-id="25780-144">File</span></span>
- <span data-ttu-id="25780-145">Svarskö</span><span class="sxs-lookup"><span data-stu-id="25780-145">Queue</span></span>
- <span data-ttu-id="25780-146">Tabell</span><span class="sxs-lookup"><span data-stu-id="25780-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25780-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="25780-147">-StartTime</span></span>
<span data-ttu-id="25780-148">Anger tiden, som ett **datetime** -objekt där säkerhets associationen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="25780-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="25780-149">Använd Get-Date cmdlet för att få ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="25780-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25780-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25780-150">CommonParameters</span></span>
<span data-ttu-id="25780-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25780-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25780-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25780-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25780-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25780-153">INPUTS</span></span>

## <span data-ttu-id="25780-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25780-154">OUTPUTS</span></span>

## <span data-ttu-id="25780-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25780-155">NOTES</span></span>

## <span data-ttu-id="25780-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25780-156">RELATED LINKS</span></span>

[<span data-ttu-id="25780-157">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="25780-157">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="25780-158">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="25780-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="25780-159">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="25780-159">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="25780-160">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="25780-160">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="25780-161">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="25780-161">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="25780-162">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="25780-162">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


