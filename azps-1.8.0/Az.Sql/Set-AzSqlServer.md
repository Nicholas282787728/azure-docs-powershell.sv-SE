---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: 24249be1d2b5b203a207d72ebd29ec691a90c39a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746491"
---
# <span data-ttu-id="29337-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="29337-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="29337-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29337-102">SYNOPSIS</span></span>
<span data-ttu-id="29337-103">Ändrar egenskaper för en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="29337-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="29337-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29337-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29337-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29337-105">DESCRIPTION</span></span>
<span data-ttu-id="29337-106">Cmdleten **set-AzSqlServer** ändrar egenskaper för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="29337-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="29337-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29337-107">EXAMPLES</span></span>

### <span data-ttu-id="29337-108">Exempel 1: återställa administratörs lösen ordet</span><span class="sxs-lookup"><span data-stu-id="29337-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="29337-109">Det här kommandot återställer administratörs lösen ordet på AzureSQL-servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="29337-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="29337-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29337-110">PARAMETERS</span></span>

### <span data-ttu-id="29337-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="29337-111">-AssignIdentity</span></span>
<span data-ttu-id="29337-112">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="29337-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="29337-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29337-113">-DefaultProfile</span></span>
<span data-ttu-id="29337-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="29337-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29337-115">-Force</span><span class="sxs-lookup"><span data-stu-id="29337-115">-Force</span></span>
<span data-ttu-id="29337-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="29337-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29337-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29337-117">-ResourceGroupName</span></span>
<span data-ttu-id="29337-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="29337-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="29337-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29337-119">-ServerName</span></span>
<span data-ttu-id="29337-120">Anger namnet på den server som cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="29337-120">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29337-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="29337-121">-ServerVersion</span></span>
<span data-ttu-id="29337-122">Anger den version som den här cmdleten ändrar till servern.</span><span class="sxs-lookup"><span data-stu-id="29337-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="29337-123">De acceptabla värdena för den här parametern är: 2,0 och 12,0.</span><span class="sxs-lookup"><span data-stu-id="29337-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="29337-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="29337-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="29337-125">Anger ett nytt lösen ord som en **SecureString** för databas Server administratören.</span><span class="sxs-lookup"><span data-stu-id="29337-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="29337-126">Använd Get-Credential cmdlet för att få en **SecureString**.</span><span class="sxs-lookup"><span data-stu-id="29337-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="29337-127">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="29337-127">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29337-128">-Taggar</span><span class="sxs-lookup"><span data-stu-id="29337-128">-Tags</span></span>
<span data-ttu-id="29337-129">Anger en ord lista med taggar som denna cmdlet associerar med servern.</span><span class="sxs-lookup"><span data-stu-id="29337-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="29337-130">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="29337-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="29337-131">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="29337-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29337-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29337-132">-Confirm</span></span>
<span data-ttu-id="29337-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29337-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29337-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29337-134">-WhatIf</span></span>
<span data-ttu-id="29337-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29337-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29337-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29337-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29337-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29337-137">CommonParameters</span></span>
<span data-ttu-id="29337-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29337-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29337-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29337-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29337-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29337-140">INPUTS</span></span>

### <span data-ttu-id="29337-141">System. String</span><span class="sxs-lookup"><span data-stu-id="29337-141">System.String</span></span>

## <span data-ttu-id="29337-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29337-142">OUTPUTS</span></span>

### <span data-ttu-id="29337-143">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="29337-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="29337-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29337-144">NOTES</span></span>

## <span data-ttu-id="29337-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29337-145">RELATED LINKS</span></span>

[<span data-ttu-id="29337-146">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="29337-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
