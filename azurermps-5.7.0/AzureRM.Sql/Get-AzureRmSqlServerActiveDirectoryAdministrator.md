---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: e782ef221474ab3a041fddc7628157fd999796d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575483"
---
# <span data-ttu-id="848ef-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="848ef-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="848ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="848ef-102">SYNOPSIS</span></span>
<span data-ttu-id="848ef-103">Hämtar information om en Azure AD-administratör för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="848ef-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="848ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="848ef-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="848ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="848ef-105">DESCRIPTION</span></span>
<span data-ttu-id="848ef-106">Cmdleten **Get-AzureRmSqlServerActiveDirectoryAdministrator** hämtar information om en Azure Active Directory (Azure AD-administratör) för en AzureSQL-server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="848ef-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="848ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="848ef-107">EXAMPLES</span></span>

### <span data-ttu-id="848ef-108">Exempel 1: hämtar information om en administratör för en server</span><span class="sxs-lookup"><span data-stu-id="848ef-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="848ef-109">Med det här kommandot får du information om en Azure AD-administratör för en server med namnet Server01 som är kopplad till en resurs grupp med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="848ef-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="848ef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="848ef-110">PARAMETERS</span></span>

### <span data-ttu-id="848ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848ef-111">-DefaultProfile</span></span>
<span data-ttu-id="848ef-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="848ef-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="848ef-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="848ef-113">-ResourceGroupName</span></span>
<span data-ttu-id="848ef-114">Anger namnet på den resurs grupp som SQL-servern har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="848ef-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848ef-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="848ef-115">-ServerName</span></span>
<span data-ttu-id="848ef-116">Anger namnet på den SQL Server som den här cmdleten får information om.</span><span class="sxs-lookup"><span data-stu-id="848ef-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848ef-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="848ef-117">-Confirm</span></span>
<span data-ttu-id="848ef-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="848ef-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="848ef-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="848ef-119">-WhatIf</span></span>
<span data-ttu-id="848ef-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="848ef-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="848ef-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="848ef-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="848ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848ef-122">CommonParameters</span></span>
<span data-ttu-id="848ef-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="848ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848ef-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="848ef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848ef-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="848ef-125">INPUTS</span></span>

### <span data-ttu-id="848ef-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="848ef-126">None</span></span>
<span data-ttu-id="848ef-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="848ef-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="848ef-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="848ef-128">OUTPUTS</span></span>

### <span data-ttu-id="848ef-129">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="848ef-129">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="848ef-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="848ef-130">NOTES</span></span>

## <span data-ttu-id="848ef-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="848ef-131">RELATED LINKS</span></span>

[<span data-ttu-id="848ef-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="848ef-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="848ef-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="848ef-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="848ef-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="848ef-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


