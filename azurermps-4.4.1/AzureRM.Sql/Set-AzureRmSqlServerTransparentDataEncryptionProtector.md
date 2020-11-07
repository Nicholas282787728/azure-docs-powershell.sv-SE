---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758257"
---
# <span data-ttu-id="cefa1-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cefa1-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="cefa1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cefa1-102">SYNOPSIS</span></span>
<span data-ttu-id="cefa1-103">Ställer in skydd mot transparent data kryptering (TDE) för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="cefa1-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cefa1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cefa1-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cefa1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cefa1-105">DESCRIPTION</span></span>
<span data-ttu-id="cefa1-106">Set-AzureRmSqlServerTransparentDataEncryptionProtector-cmdleten ställer in TDE-skyddskomponenten för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="cefa1-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="cefa1-107">Om du ändrar TDE skydds typ roteras skydds komponenten.</span><span class="sxs-lookup"><span data-stu-id="cefa1-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="cefa1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cefa1-108">EXAMPLES</span></span>

### <span data-ttu-id="cefa1-109">--------------------------Exempel 1: Ange skydds typen transparent data kryptering (TDE) till ServiceManaged--------------------------</span><span class="sxs-lookup"><span data-stu-id="cefa1-109">--------------------------  Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="cefa1-110">Det här kommandot uppdaterar en servers TDE skydds typ till tjänst hanterad.</span><span class="sxs-lookup"><span data-stu-id="cefa1-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="cefa1-111">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="cefa1-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="cefa1-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="cefa1-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="cefa1-113">--------------------------Exempel 2: Ange den transparenta typen av data krypterings skydd för Azure Key Vault--------------------------</span><span class="sxs-lookup"><span data-stu-id="cefa1-113">--------------------------  Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="cefa1-114">Det här kommandot uppdaterar en server för användning av Server Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="cefa1-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="cefa1-115">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="cefa1-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="cefa1-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="cefa1-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="cefa1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cefa1-117">PARAMETERS</span></span>

### <span data-ttu-id="cefa1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cefa1-118">-Force</span></span>
<span data-ttu-id="cefa1-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="cefa1-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cefa1-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="cefa1-120">-KeyId</span></span>
<span data-ttu-id="cefa1-121">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cefa1-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefa1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cefa1-122">-ResourceGroupName</span></span>
<span data-ttu-id="cefa1-123">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="cefa1-123">The name of the resource group</span></span>

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

### <span data-ttu-id="cefa1-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cefa1-124">-ServerName</span></span>
<span data-ttu-id="cefa1-125">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="cefa1-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="cefa1-126">– Skriv</span><span class="sxs-lookup"><span data-stu-id="cefa1-126">-Type</span></span>
<span data-ttu-id="cefa1-127">TDE skydds typ för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="cefa1-127">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefa1-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cefa1-128">-Confirm</span></span>
<span data-ttu-id="cefa1-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cefa1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cefa1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cefa1-130">-WhatIf</span></span>
<span data-ttu-id="cefa1-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cefa1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cefa1-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cefa1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cefa1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefa1-133">-DefaultProfile</span></span>
<span data-ttu-id="cefa1-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cefa1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cefa1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefa1-135">CommonParameters</span></span>
<span data-ttu-id="cefa1-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cefa1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefa1-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cefa1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefa1-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cefa1-138">INPUTS</span></span>

### <span data-ttu-id="cefa1-139">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="cefa1-139">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="cefa1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cefa1-140">System.String</span></span>

## <span data-ttu-id="cefa1-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cefa1-141">OUTPUTS</span></span>

### <span data-ttu-id="cefa1-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="cefa1-142">System.Object</span></span>

## <span data-ttu-id="cefa1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cefa1-143">NOTES</span></span>

## <span data-ttu-id="cefa1-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cefa1-144">RELATED LINKS</span></span>

[<span data-ttu-id="cefa1-145">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="cefa1-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
