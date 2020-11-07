---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: ad2a686adac7940e450d84484cd18de84ad91d3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746351"
---
# <span data-ttu-id="3dcf7-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="3dcf7-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="3dcf7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dcf7-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcf7-103">Skapar en SAS-token på konto nivå.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="3dcf7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dcf7-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dcf7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dcf7-105">DESCRIPTION</span></span>
<span data-ttu-id="3dcf7-106">Cmdleten **New-AzStorageSASToken** skapar en SAS-token för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="3dcf7-107">Du kan använda SAS-token för att delegera behörigheter för flera tjänster eller för att delegera behörigheter för tjänster som inte är tillgängliga med en SAS-token på objekt nivå.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="3dcf7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dcf7-108">EXAMPLES</span></span>

### <span data-ttu-id="3dcf7-109">Exempel 1: skapa en SAS-token på konto nivå med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="3dcf7-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="3dcf7-110">Det här kommandot skapar en SAS-token på konto nivå med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="3dcf7-111">Exempel 2: skapa en SAS-token på konto nivå för ett intervall med IP-adresser</span><span class="sxs-lookup"><span data-stu-id="3dcf7-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="3dcf7-112">Det här kommandot skapar en SAS-token på konto nivå för HTTPS-Only-begäranden från det angivna IP-adressintervallet.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="3dcf7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dcf7-113">PARAMETERS</span></span>

### <span data-ttu-id="3dcf7-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3dcf7-114">-Context</span></span>
<span data-ttu-id="3dcf7-115">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3dcf7-116">Du kan använda New-AzStorageContext cmdlet för att hämta ett **AzureStorageContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dcf7-117">-DefaultProfile</span></span>
<span data-ttu-id="3dcf7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3dcf7-119">-ExpiryTime</span></span>
<span data-ttu-id="3dcf7-120">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3dcf7-121">-IPAddressOrRange</span></span>
<span data-ttu-id="3dcf7-122">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3dcf7-123">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-123">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-124">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="3dcf7-124">-Permission</span></span>
<span data-ttu-id="3dcf7-125">Anger behörigheterna för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="3dcf7-126">Behörigheter är bara giltiga om de stämmer överens med den angivna resurs typen.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="3dcf7-127">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="3dcf7-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="3dcf7-128">Mer information om acceptabla behörighets värden finns i skapa en konto-SÄKERHETSASSOCIATIONER https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="3dcf7-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3dcf7-129">-Protocol</span></span>
<span data-ttu-id="3dcf7-130">Anger det protokoll som tillåts för en begäran som gjorts med konto säkerhets associationen.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="3dcf7-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dcf7-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dcf7-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3dcf7-132">HttpsOnly</span></span>
- <span data-ttu-id="3dcf7-133">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3dcf7-134">-ResourceType</span></span>
<span data-ttu-id="3dcf7-135">Anger vilka resurs typer som är tillgängliga med SAS-token.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="3dcf7-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dcf7-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dcf7-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="3dcf7-137">None</span></span>
- <span data-ttu-id="3dcf7-138">Serv</span><span class="sxs-lookup"><span data-stu-id="3dcf7-138">Service</span></span>
- <span data-ttu-id="3dcf7-139">Beh</span><span class="sxs-lookup"><span data-stu-id="3dcf7-139">Container</span></span>
- <span data-ttu-id="3dcf7-140">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="3dcf7-140">Object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-141">-Service</span><span class="sxs-lookup"><span data-stu-id="3dcf7-141">-Service</span></span>
<span data-ttu-id="3dcf7-142">Anger tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-142">Specifies the service.</span></span>
<span data-ttu-id="3dcf7-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dcf7-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dcf7-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="3dcf7-144">None</span></span>
- <span data-ttu-id="3dcf7-145">Object</span><span class="sxs-lookup"><span data-stu-id="3dcf7-145">Blob</span></span>
- <span data-ttu-id="3dcf7-146">Fil</span><span class="sxs-lookup"><span data-stu-id="3dcf7-146">File</span></span>
- <span data-ttu-id="3dcf7-147">Svarskö</span><span class="sxs-lookup"><span data-stu-id="3dcf7-147">Queue</span></span>
- <span data-ttu-id="3dcf7-148">Tabell</span><span class="sxs-lookup"><span data-stu-id="3dcf7-148">Table</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3dcf7-149">-StartTime</span></span>
<span data-ttu-id="3dcf7-150">Anger tiden, som ett **datetime** -objekt där säkerhets associationen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="3dcf7-151">Använd Get-Date cmdlet för att få ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcf7-152">CommonParameters</span></span>
<span data-ttu-id="3dcf7-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcf7-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dcf7-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcf7-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dcf7-155">INPUTS</span></span>

### <span data-ttu-id="3dcf7-156">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3dcf7-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3dcf7-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dcf7-157">OUTPUTS</span></span>

### <span data-ttu-id="3dcf7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3dcf7-158">System.String</span></span>

## <span data-ttu-id="3dcf7-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dcf7-159">NOTES</span></span>

## <span data-ttu-id="3dcf7-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dcf7-160">RELATED LINKS</span></span>

[<span data-ttu-id="3dcf7-161">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3dcf7-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="3dcf7-162">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3dcf7-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="3dcf7-163">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="3dcf7-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="3dcf7-164">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="3dcf7-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="3dcf7-165">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="3dcf7-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="3dcf7-166">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="3dcf7-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


