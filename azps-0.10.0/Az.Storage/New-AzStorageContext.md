---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae22e6923a03864b9371ccdf5379ef9b6bf5189d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923589"
---
# <span data-ttu-id="e749c-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e749c-101">New-AzStorageContext</span></span>

## <span data-ttu-id="e749c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e749c-102">SYNOPSIS</span></span>
<span data-ttu-id="e749c-103">Skapar en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="e749c-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="e749c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e749c-104">SYNTAX</span></span>

### <span data-ttu-id="e749c-105">AccountNameAndKey (standard)</span><span class="sxs-lookup"><span data-stu-id="e749c-105">AccountNameAndKey (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="e749c-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="e749c-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="e749c-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="e749c-107">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e749c-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="e749c-108">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="e749c-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="e749c-109">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="e749c-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e749c-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="e749c-111">Sträng</span><span class="sxs-lookup"><span data-stu-id="e749c-111">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="e749c-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="e749c-112">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="e749c-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e749c-113">DESCRIPTION</span></span>
<span data-ttu-id="e749c-114">Cmdleten **New-AzStorageContext** skapar en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="e749c-114">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="e749c-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e749c-115">EXAMPLES</span></span>

### <span data-ttu-id="e749c-116">Exempel 1: skapa en kontext genom att ange ett lagrings konto namn och en nycklar</span><span class="sxs-lookup"><span data-stu-id="e749c-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="e749c-117">Det här kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="e749c-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="e749c-118">Exempel 2: skapa en kontext genom att ange en anslutnings sträng</span><span class="sxs-lookup"><span data-stu-id="e749c-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="e749c-119">Det här kommandot skapar en kontext baserat på den angivna anslutnings strängen för kontot ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="e749c-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="e749c-120">Exempel 3: skapa en kontext för ett anonymt lagrings konto</span><span class="sxs-lookup"><span data-stu-id="e749c-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="e749c-121">Det här kommandot skapar en kontext för anonym användning för kontot med namnet ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="e749c-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="e749c-122">Kommandot anger HTTP som ett anslutnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="e749c-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="e749c-123">Exempel 4: skapa en kontext med hjälp av det lokala utvecklings lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="e749c-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzStorageContext -Local
```

<span data-ttu-id="e749c-124">Det här kommandot skapar en kontext med hjälp av det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="e749c-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="e749c-125">Kommandot anger den *lokala* parametern.</span><span class="sxs-lookup"><span data-stu-id="e749c-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="e749c-126">Exempel 5: Hämta behållaren för det lokala utvecklings lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="e749c-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="e749c-127">Det här kommandot skapar en kontext med hjälp av det lokala utvecklings arkivet och skickar sedan den nya kontexten till cmdleten **Get-AzStorageContainer** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e749c-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e749c-128">Kommandot hämtar Azure Storage-behållaren för det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="e749c-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="e749c-129">Exempel 6: Hämta flera behållare</span><span class="sxs-lookup"><span data-stu-id="e749c-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="e749c-130">Det första kommandot skapar en kontext med hjälp av det lokala utvecklings lagrings kontot och lagrar sedan kontexten i variabeln $Context 01.</span><span class="sxs-lookup"><span data-stu-id="e749c-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="e749c-131">Det andra kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten och lagrar sedan kontexten i $Context 02-variabeln.</span><span class="sxs-lookup"><span data-stu-id="e749c-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="e749c-132">Med kommandot slut får du behållare för de kontexter som lagras i $Context 01 och $Context 02 genom att använda **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="e749c-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="e749c-133">Exempel 7: skapa en kontext med en slut punkt</span><span class="sxs-lookup"><span data-stu-id="e749c-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="e749c-134">Det här kommandot skapar en Azure Storage-kontext som har den angivna lagrings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="e749c-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="e749c-135">Kommandot skapar kontexten för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="e749c-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="e749c-136">Exempel 8: skapa en kontext med en angiven miljö</span><span class="sxs-lookup"><span data-stu-id="e749c-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="e749c-137">Det här kommandot skapar en Azure-lagringsenhet med den angivna Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="e749c-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="e749c-138">Kommandot skapar kontexten för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="e749c-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="e749c-139">Exempel 9: skapa en kontext med hjälp av en SAS-token</span><span class="sxs-lookup"><span data-stu-id="e749c-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="e749c-140">Det första kommandot skapar en SAS-token med hjälp av cmdleten **New-AzStorageContainerSASToken** för behållaren med namnet ContosoMain och lagrar sedan denna token i $SasToken variabel.</span><span class="sxs-lookup"><span data-stu-id="e749c-140">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="e749c-141">Denna token är för läsa, lägga till, uppdatera och ta bort behörigheter.</span><span class="sxs-lookup"><span data-stu-id="e749c-141">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="e749c-142">Det andra kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder SAS-token som lagras i $SasToken och lagrar sedan kontexten i $Context-variabeln.</span><span class="sxs-lookup"><span data-stu-id="e749c-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="e749c-143">Med kommandot slut visas alla blobbar som är kopplade till behållaren med namnet ContosoMain med hjälp av kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="e749c-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="e749c-144">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e749c-144">PARAMETERS</span></span>

### <span data-ttu-id="e749c-145">-Anonym</span><span class="sxs-lookup"><span data-stu-id="e749c-145">-Anonymous</span></span>
<span data-ttu-id="e749c-146">Anger att den här cmdleten skapar en Azure-lagringsenhet för anonym inloggning.</span><span class="sxs-lookup"><span data-stu-id="e749c-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e749c-147">-ConnectionString</span></span>
<span data-ttu-id="e749c-148">Anger en anslutnings sträng för Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="e749c-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-149">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="e749c-149">-Endpoint</span></span>
<span data-ttu-id="e749c-150">Anger slut punkten för Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="e749c-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-151">-Miljö</span><span class="sxs-lookup"><span data-stu-id="e749c-151">-Environment</span></span>
<span data-ttu-id="e749c-152">Anger Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="e749c-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="e749c-153">De acceptabla värdena för den här parametern är: AzureCloud och AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="e749c-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="e749c-154">Om du vill ha mer information skriver du `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="e749c-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-155">-Lokal</span><span class="sxs-lookup"><span data-stu-id="e749c-155">-Local</span></span>
<span data-ttu-id="e749c-156">Anger att denna cmdlet skapar en kontext med hjälp av det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="e749c-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-157">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e749c-157">-Protocol</span></span>
<span data-ttu-id="e749c-158">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="e749c-158">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="e749c-159">-SasToken</span></span>
<span data-ttu-id="e749c-160">Anger ett SAS-token (Shared Access signatur) för kontexten.</span><span class="sxs-lookup"><span data-stu-id="e749c-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e749c-161">-StorageAccountKey</span></span>
<span data-ttu-id="e749c-162">Anger en Key för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="e749c-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="e749c-163">Denna cmdlet skapar en kontext för den parameter som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="e749c-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e749c-164">-StorageAccountName</span></span>
<span data-ttu-id="e749c-165">Anger ett namn på en Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="e749c-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="e749c-166">Denna cmdlet skapar en kontext för det konto som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e749c-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e749c-167">CommonParameters</span></span>
<span data-ttu-id="e749c-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e749c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e749c-169">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e749c-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e749c-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e749c-170">INPUTS</span></span>

### <span data-ttu-id="e749c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="e749c-171">System.String</span></span>

## <span data-ttu-id="e749c-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e749c-172">OUTPUTS</span></span>

### <span data-ttu-id="e749c-173">Microsoft. WindowsAzure. commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e749c-173">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="e749c-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e749c-174">NOTES</span></span>

## <span data-ttu-id="e749c-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e749c-175">RELATED LINKS</span></span>

[<span data-ttu-id="e749c-176">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e749c-176">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="e749c-177">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e749c-177">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


