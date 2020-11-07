---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 33b7308841fe9f9886b07eb19e14b97108cd2673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744759"
---
# <span data-ttu-id="4e9aa-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="4e9aa-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="4e9aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9aa-103">Krypterar känsliga data.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="4e9aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e9aa-104">SYNTAX</span></span>

### <span data-ttu-id="4e9aa-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="4e9aa-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e9aa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4e9aa-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e9aa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e9aa-107">DESCRIPTION</span></span>
<span data-ttu-id="4e9aa-108">Den **nya** cmdleten AzDataFactoryEncryptValue krypterar känsliga data, till exempel ett lösen ord eller en Microsoft SQL Server-anslutningssträng, och returnerar ett krypterat värde.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="4e9aa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e9aa-109">EXAMPLES</span></span>

### <span data-ttu-id="4e9aa-110">Exempel 1: kryptera en icke-ODBC-anslutningssträng</span><span class="sxs-lookup"><span data-stu-id="4e9aa-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="4e9aa-111">I det första kommandot används ConvertTo-SecureString cmdlet för att konvertera den angivna anslutnings strängen till ett **SecureString** -objekt och sedan lagras objektet i $Value-variabeln.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="4e9aa-112">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="4e9aa-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="4e9aa-113">Tillåtna värden: SQL Server eller Oracle-anslutningssträng.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="4e9aa-114">Det andra kommandot skapar ett krypterat värde för det objekt som lagras i $Value för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="4e9aa-115">Exempel 2: kryptera en icke-ODBC-anslutningssträng som använder Windows-inloggning.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="4e9aa-116">Det första kommandot använder **ConvertTo-SecureString** för att konvertera den angivna anslutnings strängen till ett säkert String-objekt och lagrar sedan objektet i variabeln $Value.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="4e9aa-117">Det andra kommandot använder cmdleten Get-Credential för att samla in Windows-inloggningen (användar namn och lösen ord) och lagrar sedan **PSCredential** -objektet i $Credential-variabeln.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="4e9aa-118">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="4e9aa-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="4e9aa-119">Det tredje kommandot skapar ett krypterat värde för det objekt som lagras i $Value och $Credential för angiven data fabrik, Gateway, resurs grupp och länkad tjänst typ.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="4e9aa-120">Exempel 3: kryptera Server namn och autentiseringsuppgifter för den länkade tjänsten för fil system</span><span class="sxs-lookup"><span data-stu-id="4e9aa-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="4e9aa-121">Det första kommandot använder **ConvertTo-SecureString** för att konvertera den angivna strängen till en säker sträng och lagrar sedan objektet i variabeln $Value.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="4e9aa-122">Det andra kommandot används för att samla in Windows-autentisering (användar namn och lösen ord) och lagrar sedan **PSCredential** **-** objektet i variabeln $Credential.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="4e9aa-123">Det tredje kommandot skapar ett krypterat värde för det objekt som lagras i $Value och $Credential för angiven data fabrik, Gateway, resurs grupp och länkad tjänst typ.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="4e9aa-124">Exempel 4: krypterar autentiseringsuppgifter för den länkade tjänsten HDFS</span><span class="sxs-lookup"><span data-stu-id="4e9aa-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="4e9aa-125">Med kommandot **ConvertTo-SecureString** konverteras den angivna strängen till en säker sträng.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="4e9aa-126">Kommandot **ny-objekt** skapar ett PSCredential-objekt med hjälp av de säkra användar-och lösen ords strängarna.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="4e9aa-127">I stället kan du använda kommandot **Hämta-autentiseringsuppgifter** för att samla in Windows-autentisering (användar namn och lösen ord) och sedan lagra det returnerade **PSCredential** -objektet i $Credential variabel enligt föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="4e9aa-128">Med kommandot **ny-AzDataFactoryEncryptValue** skapas ett krypterat värde för det objekt som lagras i $Credential för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="4e9aa-129">Exempel 5: krypterings-autentiseringsuppgifter för ODBC-länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="4e9aa-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="4e9aa-130">Med kommandot **ConvertTo-SecureString** konverteras den angivna strängen till en säker sträng.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="4e9aa-131">Med kommandot **ny-AzDataFactoryEncryptValue** skapas ett krypterat värde för det objekt som lagras i $Value för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="4e9aa-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e9aa-132">PARAMETERS</span></span>

### <span data-ttu-id="4e9aa-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="4e9aa-133">-AuthenticationType</span></span>
<span data-ttu-id="4e9aa-134">Anger vilken typ av verifikation som ska användas för att ansluta till data källan.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="4e9aa-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4e9aa-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e9aa-136">Windows</span><span class="sxs-lookup"><span data-stu-id="4e9aa-136">Windows</span></span>
- <span data-ttu-id="4e9aa-137">Basisk</span><span class="sxs-lookup"><span data-stu-id="4e9aa-137">Basic</span></span>
- <span data-ttu-id="4e9aa-138">Anonym.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-139">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="4e9aa-139">-Credential</span></span>
<span data-ttu-id="4e9aa-140">Anger Windows autentiseringsinformation (användar namn och lösen ord) som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="4e9aa-141">Denna cmdlet krypterar de autentiseringsuppgifter du anger här.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-142">-Databas</span><span class="sxs-lookup"><span data-stu-id="4e9aa-142">-Database</span></span>
<span data-ttu-id="4e9aa-143">Anger databas namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4e9aa-144">-DataFactory</span></span>
<span data-ttu-id="4e9aa-145">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4e9aa-146">Denna cmdlet krypterar data för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4e9aa-147">-DataFactoryName</span></span>
<span data-ttu-id="4e9aa-148">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4e9aa-149">Denna cmdlet krypterar data för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9aa-150">-DefaultProfile</span></span>
<span data-ttu-id="4e9aa-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4e9aa-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="4e9aa-152">-GatewayName</span></span>
<span data-ttu-id="4e9aa-153">Anger namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="4e9aa-154">Denna cmdlet krypterar data för den gateway som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="4e9aa-155">-NonCredentialValue</span></span>
<span data-ttu-id="4e9aa-156">Anger icke-Credential-delen av ODBC-anslutningssträng (Open Database Connectivity).</span><span class="sxs-lookup"><span data-stu-id="4e9aa-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="4e9aa-157">Den här parametern används endast för den länkade ODBC-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9aa-158">-ResourceGroupName</span></span>
<span data-ttu-id="4e9aa-159">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4e9aa-160">Denna cmdlet krypterar data för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-161">-Server</span><span class="sxs-lookup"><span data-stu-id="4e9aa-161">-Server</span></span>
<span data-ttu-id="4e9aa-162">Anger Server namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-163">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4e9aa-163">-Type</span></span>
<span data-ttu-id="4e9aa-164">Anger den länkade tjänst typen.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-164">Specifies the linked service type.</span></span>
<span data-ttu-id="4e9aa-165">Denna cmdlet krypterar data för den länkade tjänst typen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="4e9aa-166">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4e9aa-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e9aa-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="4e9aa-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="4e9aa-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="4e9aa-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="4e9aa-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="4e9aa-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="4e9aa-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="4e9aa-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="4e9aa-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e9aa-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-176">-Värde</span><span class="sxs-lookup"><span data-stu-id="4e9aa-176">-Value</span></span>
<span data-ttu-id="4e9aa-177">Anger det värde som ska krypteras.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="4e9aa-178">Använd en anslutnings sträng för en lokal SQL Server-länkad tjänst och en lokal Oracle-länkad tjänst.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="4e9aa-179">För en lokal ODBC-länkad tjänst kan du använda Credential-delen av anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="4e9aa-180">För den länkade tjänsten för lokala fil system, om fil systemet är lokalt för gateway-datorn, Använd lokal eller localhost, och om fil systemet finns på en annan server än gateway-datorn, Använd \\ \\ Server namn.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9aa-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9aa-181">CommonParameters</span></span>
<span data-ttu-id="4e9aa-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e9aa-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9aa-183">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e9aa-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9aa-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e9aa-184">INPUTS</span></span>

### <span data-ttu-id="4e9aa-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4e9aa-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4e9aa-186">System. String</span><span class="sxs-lookup"><span data-stu-id="4e9aa-186">System.String</span></span>

## <span data-ttu-id="4e9aa-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e9aa-187">OUTPUTS</span></span>

### <span data-ttu-id="4e9aa-188">System. String</span><span class="sxs-lookup"><span data-stu-id="4e9aa-188">System.String</span></span>

## <span data-ttu-id="4e9aa-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e9aa-189">NOTES</span></span>
* <span data-ttu-id="4e9aa-190">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="4e9aa-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4e9aa-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e9aa-191">RELATED LINKS</span></span>

[<span data-ttu-id="4e9aa-192">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="4e9aa-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


