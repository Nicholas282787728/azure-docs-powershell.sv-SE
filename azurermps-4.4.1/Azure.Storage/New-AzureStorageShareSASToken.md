---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 84f280bf5e3297796bb8b56e5a5d42e513b79e79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574762"
---
# <span data-ttu-id="c5624-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="c5624-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="c5624-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5624-102">SYNOPSIS</span></span>
<span data-ttu-id="c5624-103">Generera signatur för delad åtkomst för Azure Storage Share.</span><span class="sxs-lookup"><span data-stu-id="c5624-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5624-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5624-104">SYNTAX</span></span>

### <span data-ttu-id="c5624-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="c5624-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="c5624-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="c5624-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="c5624-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5624-107">DESCRIPTION</span></span>
<span data-ttu-id="c5624-108">Cmdleten **New-AzureStorageShareSASToken** skapar en signatur för delad åtkomst för en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="c5624-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="c5624-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5624-109">EXAMPLES</span></span>

### <span data-ttu-id="c5624-110">Exempel 1: generera ett signatur-token för delad åtkomst för en resurs</span><span class="sxs-lookup"><span data-stu-id="c5624-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="c5624-111">Det här kommandot skapar ett signatur-token för delad åtkomst för resursen som heter ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="c5624-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="c5624-112">Exempel 2: generera flera signaturer med delad åtkomst med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="c5624-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="c5624-113">Det här kommandot får alla lagrings resurser som matchar prefixet.</span><span class="sxs-lookup"><span data-stu-id="c5624-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="c5624-114">Kommandot skickar dem till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="c5624-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5624-115">Den aktuella cmdleten skapar en delad åtkomsttoken för varje lagrings resurs som har de angivna behörigheterna.</span><span class="sxs-lookup"><span data-stu-id="c5624-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="c5624-116">Exempel 3: generera en signatur för signaturer som använder en delad åtkomst policy</span><span class="sxs-lookup"><span data-stu-id="c5624-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="c5624-117">Det här kommandot skapar ett signatur-token för delad åtkomst för lagrings resursen som heter ContosoShare och som har principen med namnet ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="c5624-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="c5624-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5624-118">PARAMETERS</span></span>

### <span data-ttu-id="c5624-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c5624-119">-Context</span></span>
<span data-ttu-id="c5624-120">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="c5624-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c5624-121">Använd New-AzureStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="c5624-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c5624-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c5624-122">-ExpiryTime</span></span>
<span data-ttu-id="c5624-123">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="c5624-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="c5624-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c5624-124">-FullUri</span></span>
<span data-ttu-id="c5624-125">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="c5624-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c5624-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c5624-126">-IPAddressOrRange</span></span>
<span data-ttu-id="c5624-127">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="c5624-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c5624-128">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="c5624-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="c5624-129">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="c5624-129">-Permission</span></span>
<span data-ttu-id="c5624-130">Anger behörigheterna i token för att komma åt resursen och filerna under resursen.</span><span class="sxs-lookup"><span data-stu-id="c5624-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5624-131">-Princip</span><span class="sxs-lookup"><span data-stu-id="c5624-131">-Policy</span></span>
<span data-ttu-id="c5624-132">Anger den lagrade åtkomst principen för en resurs.</span><span class="sxs-lookup"><span data-stu-id="c5624-132">Specifies the stored access policy for a share.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5624-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c5624-133">-Protocol</span></span>
<span data-ttu-id="c5624-134">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="c5624-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c5624-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c5624-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c5624-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c5624-136">HttpsOnly</span></span>
* <span data-ttu-id="c5624-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="c5624-137">HttpsOrHttp</span></span>

<span data-ttu-id="c5624-138">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c5624-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c5624-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c5624-139">-ShareName</span></span>
<span data-ttu-id="c5624-140">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="c5624-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5624-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c5624-141">-StartTime</span></span>
<span data-ttu-id="c5624-142">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="c5624-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c5624-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5624-143">CommonParameters</span></span>
<span data-ttu-id="c5624-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5624-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5624-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5624-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5624-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5624-146">INPUTS</span></span>

### <span data-ttu-id="c5624-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c5624-147">IStorageContext</span></span>

<span data-ttu-id="c5624-148">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c5624-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c5624-149">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="c5624-149">String</span></span>

<span data-ttu-id="c5624-150">Parametern ' ShareName ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c5624-150">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c5624-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5624-151">OUTPUTS</span></span>

### <span data-ttu-id="c5624-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c5624-152">System.String</span></span>

## <span data-ttu-id="c5624-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5624-153">NOTES</span></span>
* <span data-ttu-id="c5624-154">Nyckelord: Allmänt, Azure, tjänster, data, lagring, BLOB, kö, tabell</span><span class="sxs-lookup"><span data-stu-id="c5624-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="c5624-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5624-155">RELATED LINKS</span></span>

[<span data-ttu-id="c5624-156">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c5624-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="c5624-157">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="c5624-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
